---
layout: ../../layouts/BlogPostLayout.astro
title: LBrowser, Chromium, and Your Privacy - An Honest Look
pubDate: 2025-05-15
author: Poul lorca
tags:
  - Privacy
  - Chromium
  - Open Source
---

When web privacy comes to mind, Google isn't usually the first name that inspires confidence. With a history of questionable practices and legal battles, a common piece of advice for the privacy-conscious is to steer clear of Google and its services. So, why would a browser that champions privacy, like LBrowser, choose to use Chromium, the open-source project Google initiated?

It's a fair question, and we believe in being completely transparent. Many projects aren't upfront about the rendering engines they use, which we don't think is right. So, let's dive in.

### How LBrowser Uses Chromium

LBrowser utilizes Qt WebView to display web content. Qt WebView, in turn, comes bundled with a Chromium engine (you can see more about Qt's Chromium versions [here](https://wiki.qt.io/QtWebEngine/ChromiumVersions)).

At this point, it's crucial to understand a key distinction: **Chromium is not Chrome.**
Google Chrome is a proprietary browser built *by* Google *from* Chromium. Chromium itself is an open-source project. The vast majority of modern browsers are built on Chromium, including:

* Microsoft Edge ([Wikipedia](https://en.wikipedia.org/wiki/Microsoft_Edge))
* Opera ([Wikipedia](https://en.wikipedia.org/wiki/Opera_(web_browser)))
* Brave ([Wikipedia](https://en.wikipedia.org/wiki/Brave_(web_browser)))
* Vivaldi ([Wikipedia](https://en.wikipedia.org/wiki/Vivaldi_(web_browser)))
* Epic Browser ([Wikipedia](https://en.wikipedia.org/wiki/Epic_(web_browser)))
* And many more...

Compared to Google Chrome, Chromium is significantly more customizable and manageable in terms of privacy. Its open-source nature also means it's far more auditable by the global community.

### So, Can a Chromium-Based Browser Be Secure and Private?

The answer is **yes**. Many companies and projects focused on security and anonymity build upon this foundation.

However, it's true that a browser core with significant Google involvement might still contain elements we wouldn't expect, like pings to Google services or non-user-specific telemetry that contributes to Google's data. This is a valid concern, but it's also manageable.

**LBrowser's approach is to ensure that data leaving your device only goes where *you* intend it to, without leaking to unwanted services.** This is a challenging endeavor, and we can only achieve it with community help – which is why LBrowser is open source.

The fact that Chromium is isolated within Qt's WebView gives us a greater degree of control over aspects like network requests. Our strategy involves meticulously working to channel traffic through the resilient services LBrowser integrates with (like Tor, I2P, Hyphanet, etc.), aiming to mitigate the browser's inherent telemetry through other channels.

To further guarantee or increase control over browser telemetry, LBrowser includes network modes that can be managed via Docker and Portainer. While these are services running on your machine that you *could* access with other browsers, managing their telemetry typically requires manual configuration. LBrowser aims for simplicity by controlling Chromium's telemetry through its isolated execution within the WebView, rather than just presenting a service and exposing you to data leaks via the browser's own telemetry. However, you always have the option to access the core configuration of these network modes from other browsers if you feel they better protect your telemetry.

### Why Not a Firefox-Based Engine?

This is another common question. For instance, Tor Browser mandates a Firefox-based browser. While Firefox isn't Chromium, it also faces questions today about how user data is handled. LBrowser's philosophy is that no one should force you to use a specific browser – not even under the guise of enhanced security. That's why LBrowser is a browser, but it doesn't force you to browse the networks you select *through* it (except for the standard surface web mode).

### Why LBrowser Ultimately Chose Chromium

Among many reasons, the key factors are:

1.  **It *can* be made secure:** With diligent effort, Chromium can be a foundation for a private Browse experience.
2.  **Unmatched Support & Security Patches:** It's the most widely supported open-source browser engine with the most frequent security patches. Qt itself also contributes patches to enhance its security.
3.  **Compatibility:** Other engine options often struggle with website compatibility, leading to a broken user experience.
4.  **Technical Performance:** Despite the privacy implications (which, as we've discussed, are manageable), Chromium currently offers the best option in terms of technical performance, security patching, and broad compatibility.

### What LBrowser Does (and Will Do) to Respect Your Privacy

**Currently Implemented:**

* **Transparent Business Model:** LBrowser has no hidden business model and does not sell your data to anyone. Period.
* **No Accounts:** We don't require account creation, so there's no central point to associate your activity.
* **Fully Portable:** It doesn't deeply integrate with your system files or paths.
* **Open Source:** Our code is 100% auditable by anyone.
* **No Caching (to disk):** All Browse data resides in RAM.
* **No History:** Your Browse history is not stored.
* **Ephemeral:** All session data dies when the browser is closed.
* **No Persistent Cookies:** We manage cookies to enhance privacy.
* **Proxy Use:** Utilizes proxies for connections between different network modes.
* **Uniform User Agent:** Helps to reduce a common fingerprinting vector.

**What We're Working On:**

* **Advanced JavaScript Blocking:** Granular control over JavaScript execution.
* **Fingerprinting Resistance:** Implementing measures to prevent browser fingerprinting in ways that don't cripple your Browse experience (e.g., options to disable WebGL).

### The Journey Ahead

LBrowser is in its early stages. It's important for you to know that it might not yet be as secure as we ultimately want it to be. Our primary goal is to find the right balance between user experience, ease of use, and robust privacy. After all, a super-secure browser isn't helpful if it breaks your ability to control how you navigate or what you want to see.

Everyone can contribute to this project and help guide it towards becoming even more secure. And if you feel you need an even more hardened setup right now, you can run LBrowser's network mode services (Tor, I2P, etc.) and connect to their available ports on your computer from any browser you deem more secure. There's absolutely no problem with that – it's your computer, your security, and your data.

That's what LBrowser is all about: striving for a web that is once again free and open for everyone.