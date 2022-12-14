---
date: 2022-12-16T09:35:20Z
draft: false
title: "Ubuntu - apt sources cleanup"
description: "Fix Target package is configured multiple times"
authors: ["Kieran Wynne"]
tags: ["ubuntu","apt"]
categories: ["Ubuntu","Linux"]
---


Today I discovered that a number of my Docker containers had failed, most likely due to a power outage or something. So I decided that today would be a good day to perform some server maintenance. After struggling with a slew of now-defunct Docker containers and a severe lack of storage, I started updating my packages with apt update.
I couldn't help but notice a couple `Target package is configured multiple times` issues.

After some digging, I came upon a [askubuntu](https://askubuntu.com/questions/760896/how-can-i-fix-apt-error-w-target-packages-is-configured-multiple-times/762815#762815) post (and answer).


The answer to the problem comes from David Foerster on github, and his repo [aptsources-cleanup](https://github.com/davidfoerster/aptsources-cleanup)
Simply download and run the .pyz file from the releases page and follow the prompts to fix the issues.
- Run the python script, and follow the onscreen prompts.
https://github.com/davidfoerster/aptsources-cleanup