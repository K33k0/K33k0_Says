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

I am not a fan of ads, like most. Because of this I recently setup https://github.com/revanced on my phone.

Like many phones out there youtube comes preinstalled, meaning its likely a system app. Some system apps can be disabled through the settings/appinfo. However some tricky ones, there just doesn't seem to be a way of disabling using the device itself.

This is where [ADB](https://forum.xda-developers.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/) comes into play. Now I'm not going to give a full tutorial on how to install it or on how to enable debugging on your phone. This site is about getting the commands quickly, with just a little pre-text.

Any way, once you're all set, and running `adb devices` displays a device, you can run the below.

`adb shell pm disable-user --user 0 <package to uninstall>`

That's it, done. The app is disabled.

If you're left wondering, "Okay but what is the package name?". Well there are two ways to find this, one is to install [App Inspector](https://play.google.com/store/apps/details?id=com.ubqsoft.sec) and find the package name in there.

Alternatively you can use ADB, running the following command will list all installed packages `abd shell pm list packages`.

That's all!