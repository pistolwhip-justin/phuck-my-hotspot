# Phuck My Hotspot

Share your Android phone's mobile data with other devices using Wi-Fi Direct and Android's VPN APIs, without using the carrier hotspot feature.

This is an independently rebranded copy of an upstream Android application originally published by Keggin-AI. The rebranding is intended to preserve the existing implementation and behavior; it does not independently validate upstream performance claims or carrier compatibility.

## Features retained from the upstream project

- No root required — uses Android's VpnService and Wi-Fi Direct APIs
- Wi-Fi Direct phone-to-phone, local-only USB/Wi-Fi to PC/Mac, and receiver modes
- SOCKS5 TCP and UDP support
- Cellular-bound upstream sockets
- Screen-off operation using a partial wake lock
- Built-in UDP connectivity test
- No telemetry, analytics, or trackers according to the upstream documentation

Refer to the retained technical documentation for setup instructions, architecture notes, and troubleshooting. Some historical technical material may retain original project identifiers where changing them could affect attribution or technical accuracy.

## Install the test APK

Download the test APK from the [Phuck My Hotspot GitHub Releases](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases). The initial rebranded build is debug-signed for sideload testing and is not a production/Play Store release. The new application ID allows it to install alongside the original app.

## Project contact

- **Developer:** Justin S.
- **Company:** Pistolwhip Productions LLC
- **Website:** https://pistolwhip.pro
- **Email:** justin@pistolwhip.pro
- **Support:** [GitHub Issues](https://github.com/pistolwhip-justin/phuck-my-hotspot/issues)

## License and attribution

The imported upstream project is MIT-licensed. The original license and copyright notices are retained with the imported material. Rebranding and repository-specific additions are by Justin S. / Pistolwhip Productions LLC; this does not remove or replace upstream attribution.
