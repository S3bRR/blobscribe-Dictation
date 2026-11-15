# Privacy

Blobscribe performs English speech recognition locally using its bundled model.
The app has no cloud transcription, account or built-in analytics service.
Downloading the app uses GitHub, whose own privacy policies apply to downloads
and issue reports.

## Microphone

Microphone permission allows capture from the device selected in the app. The
master switch starts enabled on launch. In always-on mode the existing voice
gate selects speech for transcription; push-to-talk mode captures while its
shortcut is held. Turn off the master switch or quit to stop dictation.

The application does not persist microphone recordings or transcript history
to a database or recording files. Current transcript/preview text exists in
memory. Settings and shortcut preferences are stored locally by macOS.

## Automatic insertion and clipboard

Automatic insertion is enabled by default for new installs and requires
Accessibility permission. It places a completed transcript on the clipboard
and sends Command–V to the active application, checking that the foreground
application has not changed. It attempts to restore previous clipboard contents
when the clipboard has not changed in the meantime. Clipboard managers and
other applications that monitor the clipboard may retain the transcript.

Clipboard mode leaves the transcript on the clipboard for you to paste.
The target application and your clipboard manager have their own data policies.

Some bare-key/modifier-only global shortcuts also require Accessibility access.
Permissions are controlled in System Settings, not bypassed by Blobscribe.

## Diagnostics and reports

Release builds disable the app's debug transcript logging. Build/evaluation
logs and test audio are not packaged in the DMG. Do not include personal audio
or transcripts in a public issue; use an intentionally recorded, non-sensitive
example if a recording is necessary and you choose to share one.
