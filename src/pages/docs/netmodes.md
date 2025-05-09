---
layout: ../../layouts/DocsLayout.astro
title: LBrowser Documentation-Net Modes
---
## Understanding Network Modes

LBrowser is designed to help you navigate beyond the conventional web. Its "Network Modes" feature is the key to easily accessing decentralized and privacy-focused networks like Tor, I2P, Zeronet, and Hyphanet directly from your browser interface.

### How It Works

This functionality is powered by **Docker containers**. LBrowser manages dedicated Docker images for each network mode. When you activate a mode, LBrowser creates a secure bridge via pre-configured ports to these containerized environments running on your system. This essentially opens a secure window from LBrowser into these specific networks, allowing you to browse them without complex manual configurations.

**Key Advantages of this Approach:**

* **Enhanced Security:** Each network runs in its own isolated container environment, providing a layer of security and preventing potential conflicts or leaks between networks and the standard web Browse session.
* **Simplified Access:** Abstracting the complexity of setting up and maintaining connections to these networks (like Tor or I2P daemons) into simple "modes" makes them accessible to users without deep technical knowledge.
* **Curated & Reviewed Images:** The Docker images used by LBrowser for these modes have been carefully curated and are continuously reviewed to minimize potential vulnerabilities and ensure a safer Browse experience within these networks.

### Setting Up Network Modes

To use Network Modes, you first need **Docker** installed and running on your system. Ensure that the `docker` command is accessible from your system's command line.

Once Docker is ready:

1.  In LBrowser, find and click the **'Net Config'** button.
2.  LBrowser will automatically begin the configuration process. This involves downloading a **Portainer** Docker image and setting up the necessary bridge network and configurations.
3.  Upon completion, a new browser tab will open, directing you to the Portainer interface. Portainer is a management UI for Docker, and LBrowser uses it to simplify the handling of the network mode containers.
4.  The first time you access Portainer, it will prompt you to set up a username and password. **This is a security measure native to Portainer.** LBrowser does **not** store or have access to these credentials; they are stored solely within the Portainer container itself.
5.  Within the Portainer interface, you will see the containers for the available network modes (Tor, I2P, etc.) already downloaded and configured. To activate a network, simply click the **'play'** button next to its container.
6.  Once a network container is running, return to LBrowser and use the **'Net Modes'** option to select the network you wish to browse through.

**Storage & Performance:**

The Docker images for all current network modes combined should occupy a bit over 1GB of storage space on your system. The number of network containers you can run simultaneously will depend on your computer's processing power and available RAM.

**Troubleshooting:**

If you encounter issues with Network Modes, a common troubleshooting step is to remove the existing network mode containers and images via the Portainer interface and then re-run the **'Net Config'** process in LBrowser. This refreshes the setup with the latest configurations and potentially newer Docker images.

<div class="flex justify-between mt-8 pt-4 border-t border-border">
    <a href="/docs/introduction" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">← Previous Section</a>
    <a href="/docs/modes" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">Next Section →</a>
</div>