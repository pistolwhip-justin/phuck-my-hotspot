# 📶 Phuck My Hotspot

![Build](https://img.shields.io/badge/build-GitHub%20Actions-blue) ![License](https://img.shields.io/badge/license-WTFPL-brightgreen)

**Share your Android phone's internet connection with nearby devices over Wi-Fi Direct.**

## 📦 Test APK

The current test build is **v5.0.5**.

- [Download the latest release APK](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases/latest)
- [All releases](https://github.com/pistolwhip-justin/phuck-my-hotspot/releases)
- [GitHub Actions builds](https://github.com/pistolwhip-justin/phuck-my-hotspot/actions)

This is a debug-signed sideload/testing APK, not a Play Store release. It uses application ID `pro.pistolwhip.phuckmyhotspot`. Device behavior must still be validated on the intended phones.

## 📋 Usage



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
