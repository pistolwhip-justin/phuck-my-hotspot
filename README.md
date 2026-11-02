# 📶 Phuck My Hotspot

![Build](https://img.shields.io/badge/build-GitHub%20Actions-blue) ![License](https://img.shields.io/badge/license-WTFPL-brightgreen)

**Share your Android phone's internet connection with nearby devices over Wi-Fi Direct.**

Phuck My Hotspot is an independently rebranded Android application based on DataNet Share. It preserves the existing sender/receiver networking implementation and includes diagnostic logging for service lifecycle, wake-lock activity, traffic counters, tunnel statistics, CPU-time snapshots, battery readings, and errors.

## 📦 Test APK

The current test build is **v5.0.4**.

- [Download the latest release APK](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest)
- [All releases](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases)
- [GitHub Actions builds](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions)

This is a debug-signed sideload/testing APK, not a Play Store release. It uses application ID `pro.pistolwhip.phuckmyhotspot`. Device behavior must still be validated on the intended phones.

## 🔎 Diagnostics

Use **EXPORT DIAGNOSTIC LOGS** in the app to save a text log through Android's document picker. Events include timestamps, elapsed time, process CPU-time snapshots, battery percentage snapshots, service/activity lifecycle, wake-lock acquire/release events, Wi-Fi Direct state transitions, and network/tunnel counters.

The logger does not intentionally record notification contents, Wi-Fi passwords, or shared credentials. Diagnostics add measurement and file-I/O overhead, so these measurements represent the instrumented build rather than a zero-overhead performance baseline.

## 🛠️ Build from source

The Android project is located at `source-import/datnet-share-v5-final/source`. The versioned GitHub Actions workflow uses JDK 17, Gradle 8.5, and Android SDK 34. It runs available debug unit tests and assembles a debug APK from committed source.

## 🧾 Upstream project and attribution

Based on [DataNet Share by Keggin-AI](https://github.com/Keggin-AI/DataNetShare). Original implementation and upstream notices are retained where applicable. Some upstream material is MIT-licensed; this repository's WTFPL notice does not remove or replace those original obligations.

Branding and repository maintenance: Justin S. / Pistolwhip Productions LLC.

- Website: https://pistolwhip.pro
- Contact: justin@pistolwhip.pro
- [Report an issue](https://github.com/pistolwhip-justin/phuck-my-hotspot/issues)

## 📜 License

[![WTFPL](logo-wtfpl.png)](LICENSE.md)

Original contributions in this repository are licensed under the [Do What The Fuck You Want To Public License, Version 2](LICENSE.md). Retained upstream components remain subject to their original license and copyright notices.

---

Last updated: 2026-11-02
