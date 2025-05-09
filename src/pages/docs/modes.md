---
layout: ../../layouts/DocsLayout.astro
title: LBrowser Documentation-Other Modes
---
## Other Modes

Beyond its core Browse and network capabilities, LBrowser includes additional modes designed to enhance your web experience while maintaining privacy and user control.

### The Ad-Free Mode

LBrowser comes with a built-in ad-free mode. This feature aims to provide a cleaner Browse experience by removing visual advertisements from websites.

* **How it Works:** This mode operates by consulting public, regularly updated databases of known advertising elements. LBrowser processes this list internally and dynamically generates a stylesheet (`CSS`) that is injected into the webpages you visit. This stylesheet instructs the browser to hide the display areas where ads would typically appear.
* **Philosophy:** While perhaps not the most aggressive ad-blocking method available, this approach is intentionally designed to be minimally invasive. It prioritizes not interfering with the underlying website's structure or business model at the network level. It does **not** control your web traffic or block requests to specific ad servers. The requests for ad content still occur (meaning the website doesn't necessarily lose an 'impression'), but the ad simply isn't rendered visible to you.
* **Benefit:** This method is generally undetectable by websites, allowing for a smoother Browse experience without triggering anti-adblock walls, while still removing visual clutter.

### Media Source Mode

The Media Source mode is a utility designed for convenient access to multimedia content on a webpage.

* **How it Works:** When you activate this mode on a visited page, LBrowser performs a local analysis of the page's content. It scans for all available multimedia resources embedded or linked within the page, such as images, videos, and audio files.
* **Functionality:** LBrowser filters the detected resources to remove duplicates and then presents you with a list of unique multimedia items found. You can then select the items you are interested in and download them directly to your device.
* **Philosophy:** Our principle here is simple: If a multimedia resource is visible to you within the browser, you should have the option to download it for personal use.
* **User Responsibility:** Please be aware that the use of this tool to download copyrighted material without permission is solely the responsibility of the user. The developer of LBrowser is not responsible for how this feature is used.

### Session Isolation and History

Privacy extends to your Browse history and session data. LBrowser handles this with a strong focus on isolation and non-persistence.

* **History Disabled by Default:** The Browse history feature is intentionally blocked and disabled by default in LBrowser. You should never see a record of visited pages in a history section.
* **Session Isolation:** All Browse sessions are isolated. Information related to your navigation within a single session (like back and forward page navigation) is stored only temporarily in your computer's RAM (Random Access Memory).
* **No Persistent Storage:** When you close LBrowser, all session data held in RAM is instantly cleared. Nothing related to your Browse session (history, visited pages, temporary navigation data) is stored persistently on your device's storage after the browser process ends.

<div class="flex justify-between mt-8 pt-4 border-t border-border">
    <a href="/lbrowser-site/docs/netmodes" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">← Previous Section</a>
    <a href="/lbrowser-site/docs/install" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">Next Section →</a>
</div>