# 📶 Phuck My Hotspot

![Build](https://img.shields.io/badge/build-GitHub%20Actions-blue) ![License](https://img.shields.io/badge/license-WTFPL-brightgreen)

**Share your Android phone's internet connection with nearby devices over Wi-Fi Direct.**

Phuck My Hotspot is an independently rebranded Android application based on DataNet Share. It preserves the existing sender/receiver networking implementation and now includes diagnostic logging for service lifecycle, wake-lock activity, traffic counters, tunnel statistics, CPU-time snapshots, battery readings, and errors.

## 📦 Test APK

The current test build is **v5.0.4**.

- [Download the latest release APK](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest)
- [All releases](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases)
- [GitHub Actions builds](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions)

This is a debug-signed sideload/testing APK, not a Play Store release. It uses the production application ID `pro.pistolwhip.phuckmyhotspot`. Device behavior must still be validated on the intended phones.

## 🔎 Diagnostics

The app records diagnostic events asynchronously to private app storage. Use **EXPORT DIAGNOSTIC LOGS** in the app to save a text log through Android's document picker.

The log is intended to help investigate long-running hotspot sessions and includes timestamps, elapsed time, process CPU-time snapshots, battery percentage snapshots, service/activity lifecycle, wake-lock acquire/release events, Wi-Fi Direct state transitions, and network/tunnel counters. It does not intentionally record notification contents, Wi-Fi passwords, or shared credentials.

Diagnostics add some measurement and file-I/O overhead. Treat measurements as observations of this instrumented build, not as a zero-overhead performance baseline.

## 🛠️ Build from source

The Android project is located at:

`source-import/datnet-share-v5-final/source`

The versioned GitHub Actions workflow uses JDK 17, Gradle 8.5, and Android SDK 34. It runs available debug unit tests and assembles a debug APK from the committed source.

## 🧾 Upstream project and attribution

This project is based on [DataNet Share by Keggin-AI](https://github.com/Keggin-AI/DataNetShare). The original implementation and its upstream notices are retained where applicable. The upstream project includes MIT-licensed material; this repository's WTFPL notice does not remove or replace those original obligations.

Branding and repository maintenance: Justin S. / Pistolwhip Productions LLC.

- Website: https://pistolwhip.pro
- Contact: justin@pistolwhip.pro
- [Report an issue](https://github.com/pistolwhip-justin/phuck-my-hotspot/issues)

## 📜 License

[![WTFPL](logo-wtfpl.png)](LICENSE.md)

This repository's original contributions are licensed under the [Do What The Fuck You Want To Public License, Version 2](LICENSE.md). Retained upstream components remain subject to their original license and copyright notices.

---

Last updated: 2026-11-02
