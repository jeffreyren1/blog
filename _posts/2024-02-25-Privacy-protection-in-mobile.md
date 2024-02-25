---
layout: post
title: Privacy Protection in Mobile
author: Jeffrey
categories: misc
banner:
  video:
  loop: 
  volume: 
  start_at: 
  image: /assets/images/oppopic/开往春天.jpg
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: [misc,android,privacy]
top:
---


## Introduction
**PRIVACY** and **CONVENIENCE** are evil twins, and there is no absolute privacy in the world. Relative balance can create a beautiful scenery. Excessive balance will destroy this beauty. If you choose to respect your privacy rights, please note that this will to some extent infringe on the rights of the corresponding service provider and may result in your service provider exercising the right to refuse to provide some or all services. Therefore, please think twice before taking action. For the convenience of decision-making, this article will briefly attach examples at the beginning of each chapter that are known to cause such situations. Of course, the improvement of privacy level will also come at the cost of sacrificing some convenience. You need to weigh the pros and cons on your own and make decisions that are deemed appropriate.

Here are some methods to protect your privacy as much as possible:

## 1. App Ops 

The reason why cancer software causes cancer is largely due to the combination of the above two factors. One of its manifestations is the excessive demand for permissions.

AppOps can provide better and more detailed permission management functions than native Android systems.You can use it on the root phone, or activate Shizuku using ADB and grant AppOps device administrator privileges to achieve the same goal.

## 2. Storage Redirect

Due to the limitations of lower version Android permission design, any application that has obtained full storage permission can read almost all content in the phone. At the same time, they can freely write various files to achieve various unexpected goals. This is often not what we want. What needs to be read can be read, and what doesn't need to be read should not be moved, nor can it be moved. This may be what we imagine.


You can use this software to achieve: the application will only place files in its own space; The application can only read its own files, as well as files that are pre-set to be readable.

## 3. AFWall+ 
AFWall+is an open-source "firewall" that can control the behavior of application networking. Root permission is required to set interception rules. It can control the communication between an application and the Internet or other local applications.




## 4. HideMyApplist 

HideMyApplist is a list of apps that can be hidden from the launcher.Some software exploit various system vulnerabilities in an attempt to obtain a list of applications installed on the phone, in order to generate a user profile. Therefore, restricting some applications from accessing the application list has become one of the important methods to balance privacy and convenience.


## 5. Ice Box

Ice Box is a utility that can freeze applications. It can be used to prevent applications from consuming resources and to prevent applications from accessing the Internet.

You can set shortcuts, automatic freeze conditions, lock screen delay, exception situations, and other functions, which are very convenient to use.




## 6. My Android Tools


Android has four main services: services, broadcast receivers, and event and content providers. In short, as the four core components of Android applications, the "Four Kings" are the cornerstone for various applications to implement various logic. However, not all components are necessary for daily use of corresponding applications. Therefore, privacy protection can be achieved by using My Android Tools to selectively disabling certain components to prevent the application from performing specific operations.


## 7. Summary

The above methods can help you protect your privacy from a system perspective. Of course, there is much more we can do!