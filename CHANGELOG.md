# Changelog

All notable changes to Phuck My Hotspot are recorded here.

## [5.0.5] - 2026-11-02

### Added
- Diagnostic event logging for app/activity and foreground-service lifecycle.
- Wake-lock acquisition and release events.
- Wi-Fi Direct state observations.
- Sender traffic counters and receiver TUN/tunnel statistics.
- CPU-time and battery-percentage snapshots on diagnostic events.
- In-app export of diagnostic logs to a text file.

### Changed
- Rebranded the application as **Phuck My Hotspot**.
- Restored the production application ID for the new repository.
- Promoted the diagnostic instrumentation into the production code line.

### Notes
- Debug-signed APK for sideload testing.
- Instrumentation adds some overhead; long-duration device testing is still required.
- No network-forwarding or retry optimization is included in this release.
