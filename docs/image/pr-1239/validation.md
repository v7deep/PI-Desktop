# Notification sound visual validation

Candidate: `6fc06768aa90dcdb6a9dff42427673a608cde2f7`

Base main: `589e5803a7a9f4ebf7ec1e8849c43e44b4a198f7`

Workflow: https://github.com/v7deep/PI-Desktop/actions/runs/39226482549

Result: 64 related tests and the isolated Electron sound-settings journey passed.
The production SettingsPage, store, controls and built CSS run in sandboxed Electron.
Only the preload boundary is mocked; settings persist in fixture Chromium localStorage.
The journey covers upload, playback, mode switching, invalid/oversized input,
save failure/retry, and restoration across two Electron processes.
Host database persistence, native notification delivery and audible output remain outside this fixture.

The images are Electron capturePage output with Simplified Chinese settings.
