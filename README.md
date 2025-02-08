# Expo Constants.deviceId returns null intermittently

This repository demonstrates a bug where Expo's `Constants.deviceId` API returns `null` unexpectedly. The issue is intermittent and seems to be related to the development environment (simulators, emulators) and app rebuilds.  This can cause problems in applications that rely on a persistent, unique device ID.

## Bug Reproduction

1. Clone this repository.
2. Run `expo start`.
3. Observe that `Constants.deviceId` may return `null` on app launch, simulator restarts, or after a rebuild.

## Solution

The provided solution implements a more robust approach to obtaining a device ID, using a combination of `Constants.deviceId` and local storage to handle cases where `Constants.deviceId` is initially `null` and to retain the ID between app sessions. 