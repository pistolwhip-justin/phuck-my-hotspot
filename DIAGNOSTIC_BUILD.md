# Phuck My Hotspot — Diagnostics

## Purpose

Diagnostic instrumentation is now part of the main production code line. This document describes the diagnostic capability included with Phuck My Hotspot.

## Instrumentation

- App foreground/background and activity lifecycle.
- Sender and receiver service commands and lifecycle.
- Sender and receiver partial wake-lock acquisition/release events.
- Wi-Fi Direct state transitions without SSID/password details.
- Sender traffic-stat callback values.
- Receiver TUN loop statistics at its existing cadence, including active TCP flow count, packet count, TCP SYN count, and byte counters.
- Timestamp, elapsed realtime, process CPU time, battery percentage when Android exposes it, and event fields.
- Bounded private log storage with one previous log file.
- In-app export to a user-selected text file.

The instrumentation observes existing code paths. It does not intentionally change wake-lock policy, packet forwarding, retry policy, socket buffers, or statistics timing. Logging itself adds some overhead and should be considered when interpreting measurements.

## Collecting logs

1. Install Phuck My Hotspot on the sender or receiver phone.
2. Reproduce the test condition and let the session run for the intended duration.
3. Open the app and tap **EXPORT DIAGNOSTIC LOGS**.
4. Save the text file and review it before sharing. The logger avoids Wi-Fi Direct credentials, but logs may still contain operational metadata.

Logs remain in private app storage until exported. Uninstalling the app removes its private logs unless exported first.

## Release and validation

The production app is built from the main branch using the versioned release workflow. A successful build and automated test run do not replace installation and long-duration testing on the actual devices.
