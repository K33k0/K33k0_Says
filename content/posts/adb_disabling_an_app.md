+++
draft = false
date = 2022-12-07T22:14:26Z
title = "ADB: Disable an app"
description = "How to disable those annoying system apps"
slug = ""
authors = ["Kieran Wynne"]
tags = ["android","system","apps"]
categories = ["android","snippet"]
externalLink = ""
series = []
+++

Like most people, I dislike advertisements. As a result, I just installed https://github.com/revanced on my phone.

YouTube comes preinstalled on numerous phones, indicating that it is most likely a system app. Some system apps can be turned off via settings/appinfo. However, some apps are stubborn and cannot be blocked in this manner.

This is where [ADB](https://forum.xda-developers.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/) steps in. Now, I'm not going to go into detail about how to install it or enable debugging on your phone. This webpage is all about getting the commands quickly and with as minimal pre-text as possible.

In any case, after you're all configured and `adb devices` displays a device, you can execute the following.

`adb shell pm disable-user --user 0 <package to uninstall>`

That's it; you're done. The app has been deactivated.

If you're thinking, "Okay, but what's the package name?" There are two ways to find this. The first is to install [App Inspector](https://play.google.com/store/apps/details?id=com.ubqsoft.sec) and look for the package name.

Alternatively, you can use ADB; the command `abd shell pm list packages` will list all installed packages.

That's it!
