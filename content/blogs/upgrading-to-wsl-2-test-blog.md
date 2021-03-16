---
title: Upgrading to Wsl 2 (Test Blog)
banner: /assets/uploads/banner.jpg
banner_source: https://unsplash.com/@cbpsc1
---
This blog is a testing blog. Half of the blog is gibberish, I only kept this blog because I don't have right now time to write a real one.

Sed ut perspiciatis unde omnis:

1. Press the Windows + R keys
2. Type `winver` in Run window

At vero eos et accusamus et iusto odio dignissimos ducimus 1:

1. Open PowerShell
2. Check the version with `wsl -l -v`\
   placeat facere possimus, omnis voluptas assumenda estl 1
3. Update the version with `wsl --set-version Ubuntu 2`

> Aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates

Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae 2,.

- - -

Rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta:

```terminal
Conversion in progress, this may take a few minutes...
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.
For information please visit https://aka.ms/wsl2-install
```

Molestias excepturi sint occaecati cupiditate non provident, similiquet:

1. Type `Windows features` in usual window search option at the bottom left on taskbar
2. Now, find and check Virtual Machine Platform from those options

Itaque earum rerum hic tenetur a sapiente delectus

- - -

Nam libero tempore, cum soluta nobis est.

The problem now is with hyper-v. I know the error message doesn't exactly say that but I've found, hyper-v is a required when running Wsl 2. If you want to read more about it, Refer this [link](https://github.com/microsoft/WSL/issues/5363)

Now to enable that, you can just do it from the same windows features menu or you can type these commands in powershell:

```powershell
DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V
bcdedit /set hypervisorlaunchtype aut
```

Restart your system when the process finishes.

Try to run the update command again,

```powershell
wsl --set-version Ubuntu 2
```

If it worked, wsl 2 is running successfully.

- - -

But again if you get an error which is looking like this, then:

```terminal
Conversion in progress, this may take a few minutes...
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
The RPC server is unavailable.
```

So, now there are 2 ways to fix this,

1. Reinstall the OS (distro), I wouldn't really call this a fix but we can get rid of the error
2. Enable DNS Client service on your system

Now to enable the DNS client, it is probably best if you follow this [link](https://wintechlab.com/enable-disable-dns-client-service/)

In this link, I had the same issue they have shown where the service was greyed out and I was unable to start it. To resolve it, I took the steps mentioning regedit.

[![alt text](https://pranavmalvawala.com/static/4492a13e6bea2125a03abbec8fb9355e/36dbb/regedit.jpg "regedit")](https://pranavmalvawala.com/static/4492a13e6bea2125a03abbec8fb9355e/1fe05/regedit.jpg)

In that I found my start setting already showed 4 so I decided to make it 2 so that it can be automatic and restarted my PC.

Again I tried update command and this time It worked perfectly

1. `wsl --set-version Ubuntu 2`

But it took hours to finish. At one point I even thought of just stopping it cause there was no feedback that is it still working or is the process just stuck. But I found if you see task manager and the disk usage is around 100% and a process named `vmmem` is running then yes conversion is still working.

If you dont want to wait that long then you should just consider uninstalling the current ubuntu and reinstall it again. I found this [link](https://www.digitalocean.com/community/posts/trying-the-new-wsl-2-its-fast-windows-subsystem-for-linux) easy to follow, I suggest taking backup of projects before doing this, cause everything will be cleared.

> Everything is new now, so why don't you try one more thing. You must have noticed that your whole Ubuntu is on your main system drive if you use it for a long time, it can take up a huge amount of space.\
> \
> I found that it is possible to move distro to another drive. We can do it with running some commands in powershell. But I've found [this](https://github.com/pxlrbt/move-wsl) amazing script that can do it very easily. Go head and try it. It worked perfectly for me.

Let me know, If you still have some problems following any of the part or maybe got a completely different kind of an error. I'd be happy to help.