---
author: "Chris Walz"
date: 2020-05-25
draft: false
linktitle: Books that changed how I see the world
menu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: How to secure you website as a startup
description: There are some simple easy steps to take 
weight: 10
---


Whether it’s the difficulties of building out new features or finding the coveted product-market fit, running a startup is hard. With so much to do, security can sometimes take a backseat but remains a danger lingering in the back of your mind.

Thankfully there are some simple, fundamental steps that you can take to secure your website or app.

# Encryption

The first and most critical step in securing all communications to your app is using HTTPS. Reverse proxies like Caddy (my personal favorite) or Nginx make it relatively easy to integrate HTTPS into your website.

# Security Rules

Security rules/firewalls are a simple and effective way to mitigate certain attack vectors. For example, having an open ssh port (22) can make it easy for a hacker to brute force their way into executing code directly on your server (RCE attack).

The default AWS security groups allow everything which, to put it simply, isn’t ideal. Here’s an example of what would be preferred for most websites for INBOUND (Ingress) requests. Allows only HTTPS connections.

For OUTBOUND requests, you’ll probably want to allow nothing or perhaps HTTPS if your server relies on third-party web APIs.

Here’s some additional information on using security rules for your website on AWS.

# Use an automated security grader

It’s important to regularly audit and scan your app for vulnerabilities. ReconBuddy makes it easy to give your website a quick security checkup. Plug in your website link or a link to your app. ReconBuddy will then check for attack vectors such as: using HTTP, open ports, bad CORS policies and even fuzzing attacks.

# Security is a work in progress

Security is hard and your website’s security will never be perfect. The fact that you’re reading this article means you’re mindful of security and that will pay dividends in the future.

>This post was written by Chris Walz. Chris is a software engineer who’s worked in everything from FinTech to Construction to Security. He also had a brief stint at Google where he and his fellow team members collaborated to make the internet faster. He loves to experiment with bleeding-edge technologies and automation, not to mention he has a mean serve in table tennis.
>


