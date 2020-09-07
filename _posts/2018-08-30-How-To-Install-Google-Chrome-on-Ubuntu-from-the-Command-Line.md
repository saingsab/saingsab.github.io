---
title: How To Install Google Chrome on Ubuntu from the Command Line
layout: post
categories: [Technology, how to, linux]
image: /assets/img/2e706e67.png
description: "How to tips"
---
![google chrome](/assets/img/2e706e67.png)

I have installed new Ubuntu Operating System on my laptop during the trip to ShenZhen. For those who never been here it's pretty easy to install Google Chrome by download its from Google website.

As everyone know very well that China is one of a very restricted Internet connect there is no google here. So it's a bit challenge to install Google Chrome here. There is another possible way to install Google Chrome and I decide to write an article for those who want to do it correctly.

Let's jumping to bellow step

### Step: 1 Add Source List
Press CTRL+ALT+T to open a terminal or you can open any terminal as your favorite once, then edit sources.list file with any favorite text editor I love Nano so i'm going to do with it. You should have done it with super user privilege.

```
sudo nano /etc/apt/sources.list
```
Use the down arrow key to scroll to the bottom of this file. Add the following APT line at the end of the file.

```
deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main
```

![google chrome](/assets/img/6f757263655f6c6973742e706e67.png)


### Step: 2 Add Add Linux Signing Key
In Nano text editor in order to save the file we need to press Ctrl+O, then Enter to confirm. press CTRL+X to exit out of this file of you can make it's faster by CTRL + X and Enter. After that, enter the following command to download Google’s signing key.

```
wget https://dl.google.com/linux/linux_signing_key.pub
```
Then use apt-key to add with sudo privilege to your keyring so the package manager can verify the integrity of Google Chrome package.

```
sudo apt-key add linux_signing_key.pub
```

### Step: 3 Install Google Chrome
Lets update package list before install the stable version of Google Chrome.

```
sudo apt update
sudo apt install google-chrome-stable
```
Installing Google Chrome browser on Ubuntu is pretty easy! As always, if you found this post useful or any error please let's me know on commend below.