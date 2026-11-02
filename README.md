# 📶 Phuck My Hotspot

[![Build](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions/workflows/release-5.0.5.yml/badge.svg)](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions/workflows/release-5.0.5.yml) [![Latest Release](https://img.shields.io/github/v/release/pistolwhip-justin/phuck-my-hotspot?label=latest%20release)](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest) ![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white) [![License](https://img.shields.io/github/license/pistolwhip-justin/phuck-my-hotspot)](LICENSE.md) [![Last Commit](https://img.shields.io/github/last-commit/pistolwhip-justin/phuck-my-hotspot)](https://github.com/pistolwhip-justin/phuck-my-hotspot/commits/main)

**Share your Android phone's internet connection with nearby devices over Wi-Fi Direct.**

## 📦 Test APK

The current test build is **v5.0.5**.

- [Download the latest release APK](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest)
- [All releases](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases)
- [GitHub Actions builds](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions)

This is a debug-signed sideload/testing APK, not a Play Store release. It uses application ID `pro.pistolwhip.phuckmyhotspot`. Device behavior must still be validated on the intended phones.

## 📋 Usage

### Installation

1. Open the [latest Phuck My Hotspot release](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest).
2. Under **Assets**, download **PhuckMyHotspot-v5.0.5-debug.apk**. If a newer release is available, download the APK attached to that release instead.
3. Open the downloaded APK from your browser's download notification or your device's Downloads folder.
4. If Android asks you to authorize the app used to open the APK to install unknown apps, allow installation for that source and continue. The exact setting location varies by Android version and device.
5. Review the installation prompt and install the app.

**Important:** This APK is distributed directly through GitHub. It is not a Google Play Store release and has not been verified or approved through the Play Store review process. Google Play Protect may display an unverified-app warning during installation. If you have obtained the APK from the official release page linked above and choose to proceed, select **Install anyway** when that option is presented. Do not proceed with an APK from an untrusted or different source.

### Phone Sharing Internet

Use the phone with the internet connection as the sharing device.

1. Turn on Wi-Fi in **Phone Settings > Connections**. A mobile data connection is not required for the Wi-Fi Direct connection itself, but the sharing phone must have an internet connection available to share.
2. Open **Phuck My Hotspot**.
3. Tap **Start Sharing (Wi-Fi Direct)**.
4. Wait for the status to change to indicate that sharing is active.

If the status remains **Starting** for more than a few seconds, tap **Stop**, close and reopen the app, then tap **Start Sharing (Wi-Fi Direct)** again.

### Phone Receiving Internet

Install Phuck My Hotspot on the receiving phone as described above. The receiving phone connects to the sharing phone over Wi-Fi Direct and then joins the Wi-Fi network details provided by the sharing phone.

1. On the receiving phone, open **Settings > Connections > ⋮ (three-dot menu) > Wi-Fi Direct**.
2. Select the sharing phone from the available devices and complete the connection.
3. Return to the receiving phone's available Wi-Fi networks.
4. Find the Wi-Fi network listed in the **Phuck My Hotspot Credentials** section on the sharing phone.
5. Select that network and enter the password shown in the sharing phone's credentials.
6. Open **Phuck My Hotspot** on the receiving phone and tap **Start Receiving**.
7. Wait for the status to show **Active**.

If the status remains **Starting** for more than a few seconds, tap **Stop**, close and reopen the app, then tap **Start Receiving** again.

### Diagnostic testing

The startup process and battery usage are current areas of investigation. The diagnostic data collected by this test build is intended to help identify and address delays or failures during startup, as well as measure battery impact, so these areas can be improved in future releases. To share diagnostic information, use **EXPORT DIAGNOSTIC LOGS** in the app and provide the exported text file when reporting an issue.

## 🔎 Diagnostics

Use **EXPORT DIAGNOSTIC LOGS** in the app to save a text log through Android's document picker. Events include timestamps, elapsed time, process CPU-time snapshots, battery percentage snapshots, service/activity lifecycle, wake-lock acquire/release events, Wi-Fi Direct state transitions, and network/tunnel counters.

## 👀 Privacy

The logger does not record device ID, notification content, Wi-Fi passwords, shared credentials, or any personal data. Diagnostics add measurement and file-I/O overhead, so these measurements represent the instrumented build rather than a zero-overhead performance baseline.

## 🛠️ Build from source

The versioned GitHub Actions workflow uses JDK 17, Gradle 8.5, and Android SDK 34. It runs available debug unit tests and assembles a debug APK from committed source.

## 📜 License

[![WTFPL](logo-wtfpl.png)](LICENSE.md)

This repository is licensed under the [Do What The Fuck You Want To Public License, Version 2](LICENSE.md).

---

Last updated: 2026-11-02
