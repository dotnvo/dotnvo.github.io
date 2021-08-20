---
layout: post
title: Devolutions Remote Desktop Manager Review
cover-img: /assets/img/
thumbnail-img: /assets/img/
share-img: /assets/img/
tags: [reviews, RemoteDesktopManager, Software]
comments: true
---

For the last couple of months, my team has been transitioning to Remote Desktop Manager, from RoyalTS. I&#39;ve used Remote Desktop Manager as well in the past in current situations and it&#39;s been a product I&#39;ve simply enjoyed using. I decided it was worth writing a more in-depth review.

# Overview

[Remote Desktop Manager](https://remotedesktopmanager.com/) is, as the name implies, an application that helps with Remote Desktop management. It does a lot more than manager your windows RDP sessions. IT professionals everyday face the challenge of streamlining access to resources. Depending on use case, some users may not be as tech savvy, but still require access to several systems where remote desktop is needed. Remote Desktop Manager aims to control the chaos, with this product, providing a platform that is intuitive, scalable, and overall easy to use. There are some other products that Devolutions have built that integrate directly into this product as well.

To get started, you download/install Remote Desktop Manager, and you&#39;ll automatically have a local data source generated for you. This is a local database that stores sessions. You then can create &#39;sessions&#39; which are often connections to a remote session. You can also create things like folders, etc. for organization. A &#39;session&#39; can be an RDP session, or it can be any number of other remote technologies RDM supports, via direct integration or via add-ons. Depending on the version you use, you can create and connect to advanced data sources, which is where the real fun begins. With advanced data sources, you gain the ability to really centralize sessions, and can fine tune ACLs and controls for users. Remote Desktop Manager uses an idea called &#39;vaults&#39; to organize your sessions

# Pricing

RDM has a free version and paid version. The free version is still feature rich and incredibly useful. The paid version is called &#39;Enterprise Edition&#39; and comes with some [additional functionality](https://remotedesktopmanager.com/compare). Their licensing model comes in a few flavors; Single User, Site, Country, and Global. Most folks will probably do Single user or site license.

# Features

Frankly, there&#39;s too many features to go through for a short review. There&#39;s a ton of functionality and I&#39;m going to talk a bit about a few of my favorite features I use, including some add-ons we&#39;ve made use of. Please note there are a ton of awesome features that aren&#39;t covered here.

**Synchronizers** : These are ways to synchronize data. For example. You can setup 1 or more synchronizers to look at AD and pull in computer objects. In tandem with templates and a centralized database, this is an incredible powerful way to always have up to date sessions. This could be used for end users you support, or for your own team. We have several set up. There are additionally ways to setup CSV synchronizers if needed, which are completely customizable.

**PowerShell Module** : RDM includes a PowerShell module that lets you interact with your database sources. Honestly, the GUI is great; the bulk edit actions and being able to change things on multiple sessions is something I do use all the time, but our team often has a need to automate tasks and we enjoy using code and GitHub to make this happen. This lets you do things the same way, every time. We also share code snippets internally via Teams, Gists, or scratch repos.

**Addons** : Like many places, our systems are stored in a multitude of environments. There are wonderful add-ons that we make use of some which work with features like synchronizers, to help keep all these sessions in one place. We especially make use of the vmWare and iLO add-ons. This means we don&#39;t need to keep spreadsheets of iLO sessions, etc.

**Custom Fields** : While we are still exploring the use of the custom fields feature, this is powerful. With custom fields you can add on metadata to sessions, which would let you act on things in bulk. For example, one could perhaps use custom fields to help track patch groups so when patch Tuesday comes around, there&#39;s an organized flow to ensure we&#39;re checking that systems are coming back up properly.

# Navigation and Feel

The RDM user interface is highly customizable. The default view will fit most needs, but you can change most aspects to suite you. Because of this, the interface feels great, because you can change most things you may not like or perhaps have a preference. Many remote desktop managers will have a similar feel but the real power in RDM is that it is so customizable, and you can do things dynamically. For example, I like organizing my open RDM sessions based on some criterion. I&#39;m able to do this easily with tab groups and setting up templates. This lets me do groups of sessions by domain, or even by session type if desired.

# Overall Impressions and Conclusion

My goal was to keep this review under 1000 words, which I&#39;m quickly approaching. Overall, I&#39;m impressed with this software. There&#39;s so much more to test, review, and play with that I couldn&#39;t possibly review its full functionality without months of testing. That said, the fact that the free software comes with so much functionality, and the paid variant improves upon that is incredible. The power in this software is real, and Devolutions has taken a fantastic approach to making a simple product with advanced functionality. I believe any person can get started with this software and figure it out in a short amount of time, but I do believe it offers so much that to truly master it, one would need to use it for a while. I think this leads to a product that is easy to get started with, and with time you can master workflows using RDM as a tool to further your goals in IT. I can honestly say, controlling the chaos is something RDM helps with.