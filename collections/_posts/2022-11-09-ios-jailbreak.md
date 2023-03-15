---
layout: post
title: "[iOS Application Security] Jailbreak 12.4 and SSL pinning bypass <br> <br>  How to set up your iOS Testing Lab"
date: 2018-12-29T10:26:40+10:00
authors: ["Yogendra Jaiswal"]
categories:
  ["ios Hacking", "iOS Pentest", "Jailbreak", "Mobile Application Testing"]
tags: ["Cyber Security Blog"]
thumbnail: "/assets/images/blog_images/ios_12.png"
image: "/assets/images/blog_images/ios_testing.png"
---
Hello Everyone — Long time no see!

It’s been a long time since I published my last blog so I’ve decided to come up with a good topic since there are many questions being asked around Jailbreak and how to bypass SSL pinning. This version of the blog I’ll explain how to jailbreak iOS 12.4 and bypass SSL pinning. This will give you a decent idea on how to set up your iOS testing lab.

Surprisingly, this is the first time in 4 years a public version of iOS is Jailbreakable 12.4. In the most bizarre turn of events, you can almost do this without a computer. From iPhone 6 all the way to the iPhone 10, so without further ado, I am going to dive into the technical details and show you how to practically jailbreak your iOS without a computer.

### Disclaimer
This blog post is only meant for educational purposes and security research. Please note that you might lose all the data from the device, so make sure you have backed it all up beforehand.

## Unc0ver

Unc0ver v3.5.0 can jailbreak iOS 12.4 on A7-A11 devices, but A12(X) devices are still excluded at this time. Pwn20wnd also adds that while the jailbreak works on iOS 12.4, the success rate is lower than it was on previous versions of iOS. 

<a href="https://www.idownloadblog.com/2019/08/18/unc0ver-jailbreak-ios-12-4/"> unc0ver Jailbreak iOS 12.4 Link </a>


unc0ver jailbreak for iOS 11.0–12.4. You can check to see if your device can be jailbroken using the following website: [https://canijailbreak.com](https://canijailbreak.com)

## JailBreaking —

Jailbreaking is generally are of two types. Jailbreaking totally depends upon the iOS version your device is using. 

## 1. Tethered

Tethered jailbreaks require the iOS device to be connected to a computer while it is booting. If it is booted without a computer connected, it will not boot up. These kinds of jailbreaks are usually based on exploits of the Boot ROM, LLB or iBoot. While these jailbreaks are hard for Apple to patch, they are quite inconvenient to its users.

## 2. Untethered

Untethered jailbreaks do not need the iOS device to be connected to a computer during bootup, making them very user-friendly. Usually, the device is jailbroken once by connecting it to a computer that then exploits a vulnerability to patch the kernel.

Ref: [https://promon.co/security-news/ios-jailbreak/](https://promon.co/security-news/ios-jailbreak/)

## Jailbreaking iPhone 7 with iOS 12.4

Checking your iOS version

```
Settings -> General -> About
```

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*CuYzzRJI8gysXNlC767AZw.png" />
 

The testing environment used for jailbreaking

if your devices are compatible with Jailbreak then you should have developer's account.

You may enroll for a developer’s account via [https://developer.apple.com](https://developer.apple.com
)

### Installing Cydia Impactor

Cydia Impactor is a GUI tool for working with mobile devices. It has features already but is still very much a work-in-progress. It is developed by saurik.

Downloading & Installing Cydia Impactor. (Developers Account Required)

### Cydia Impactor

Note: Cydia requires your Apple ID and password so using a newly created Apple ID is highly recommended.

Download IPA from here [https://github.com/pwn20wndstuff/Undecimus](https://github.com/pwn20wndstuff/Undecimus) but please make sure you are using the latest release. As of now, v3.5.5 is the latest version.

Drag the IPA file and drop it into the impactor, then click on start.his will prompt you for the Apple ID username and password.

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*oV0OnwSjXN9inDTvsek9Ug.png" />
 
  <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*RpFgO_3QT4KHDRbw0yhwqA.png" />

Before proceeding to jailbreak, please restart your device then activate the airplane mode.

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*de9xvnaVjyweWcgHbnYXUw.jpeg" />
 
Open unc0ver app and click on jailbreak

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*iHJxDJuOOV0kCl3GofOzMg.png" />
 
  <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*e8txDAIwipWaV2B3iKG4vA.png" />
  
   <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*p_r8VaHIlXbLn9SacACcFQ.png" />
  
   <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*WkfI2u2jhNPrpxQaMiDcOw.png" />

Verify the Unc0ver App

```
Settings → General → Profiles & Device Management → email@company.com
```

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*3SwNAwsmn57nCFMwsQW1tg.png"/>
 
  <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*TAuSBDjwqYJymUcWsjaXNg.png"/>
  
  
 Your devices may restart multiple times so you will likely need to click on jailbreak for about 2–3 times for a complete jailbreak.

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*quFrkI8yp-Hs99tCDdTAeQ.png"/>

Once your device is jailbroken, you will get Cydia as you can see below.

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*2sddQwYPTyyvXcDuGmDehA.png"/>
 
  <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*2sddQwYPTyyvXcDuGmDehA.png"/>
  
Congratulations! Your devices in now jailbroken using Unc0ver.

### Burp Suite Free/Pro — Downloading and configuring


```
Setting Proxy lister — Proxy → Options → Proxy Listener → Add
Bind to port: 8XXX
Bind to address : All interfaces (192.168.X.X)Click “Ok”

- Note: Ip ranges may vary in your device
  ```

 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*OS_hF13ON7KHP6hrxa4VoQ.png"/>  
 

  
  <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*nn4QOqDI060ZObRQ6vX05A.png"/> 

```
Settings → wifi → (i) from connected network → Configure Proxy → Manual
Server : 192.168.1.6
Port: 8082
```
<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*QYB8z0rBzBM2Zw-NNj5yDA.png"/>  


Now select Configure `Proxy → Manual`



<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*fWN48DAr5DzoTTzA8LTPrQ.png"/>


<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*gosyo51LPIPOc1FpiV5nZg.png"/>


Now save the configuration then open the browser and visit http://burp in order to download the Portswigger CA Certificate and configuration.


<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*4l6XFJmR6u4CNG55z5Gisg.png"/>

Tap on CA Certificate to download the certificate.

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*U5w_FxcViSD-TYPpLsxIww.png"/>

Allow downloading of the configuration file.

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*JlrKLdGDgI5TZ17ayehVwA.png"/>

Select the device in which you wish to install the certificate.

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*9Ne6r0KHHEzrg601k1MeQQ.png"/>
 
 
Now, on your iPhone, go to:

```
Settings → General → Profiles & Device Management
```
<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*V5I6T-IzPL9GxOlv1g088w.png"/>

```
Profiles & Device Management → Portswigger CA
```
<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*yLYX2ctpIYOf9DpM1a0TxQ.png"/>

Install the Portswigger CA Certificate

### SSH to the iOS device

SSH is the secure shell used to connect to different machines.

1. Finding the IP address of the device.

### Settings → Connected Network → Click on [i]

The IP address of the device — 192.168.2.41

2. Available users on the iOS device are the following:

```
mobile — default password — alpine
root — default password — alpine
```

Connecting as mobile and getting root privileges.
```
ssh mobile@192.168.2.41
password=alpine // you should change it using passwd utility
```

OR

You can use Cyberduck on the other hand.

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*ygPdAjiL9mIc0Dx633N4fQ.png"/>

### Installing SSL KILL Switch 2

We will use Blackbox tool to disable SSL certificate validation — including certificate pinning — within iOS and OS X Apps. The second iteration of

[https://github.com/iSECPartners/ios-ssl-kill-switch](https://github.com/iSECPartners/ios-ssl-kill-switch)

[nabla-c0d3/ssl-kill-switch2](https://github.com/nabla-c0d3/ssl-kill-switch2)


The latest version as of now is v0.13. You can download the deb file from:
<a href="https://github.com/nabla-c0d3/ssl-kill-switch2/releases"> Github Link </a>

or direct download the version 0.13 from:

<a href="https://github.com/nabla-c0d3/ssl-kill-switch2/releases/download/0.13/com.nablac0d3.sslkillswitch2_0.13.deb">Click here to download ssl kill Switch2</a>
 


## Installation
The following dependencies should be installed using Cydia:

* Debian Packager

* Cydia Substrate

* PreferenceLoader

<b>Install MTerminal form Cydia</b>

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*uWrwolYSODRhRYJSibcOUg.png"/>

Open the MTerminal

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*WeB59p02a-HCWCNdVxouBA.png"/>

Enter Command SU

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*ktEoIqeg6W-jdnl3g6MVog.png" />
  
Enter Password — alpine

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*2VjZw5sNqEvpw2qWuGJzNQ.png" />
    
Type Command “ls” to view the files

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*b-pgf-3csUfqD6BQaTttiQ.png"/>

Type command

```
dpkg -i <package_name>.deb

```

This will install the package ssl.deb

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*FsTfUMo_Ty3wgTjVSIwdxg.png"/>

Goto Settings → Look for “SSL kill switch 2”

<img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*nbe5PdUVlvjXaC6T9Mie9g.png"/>
 
 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*8TD7a2mQtyxNc1KuKkVxKA.png"/>
 
 Now you can intercept the traffic of any iOS application.
 
 <img alt="Jekyll Atlantic Logo" src="/assets/images/blog_images/1*79lWM_ELXY--G686f3xApA.png"/>
 
 If you have any query or question just DM on Twitter [https://twitter.com/vulnh0lic/](https://twitter.com/vulnh0lic/), I will be happy to assist.
 
 Until next time!
