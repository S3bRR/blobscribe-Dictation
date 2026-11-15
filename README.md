<p align="center"><img src="assets/Blobscribe.png" width="112" alt="Blobscribe icon"></p>

# Blobscribe

Free, offline English dictation for Apple Silicon Macs.

Speak and have text inserted into the text box you are working in. Blobscribe
lives in the menu bar, with push-to-talk and always-on modes, configurable
hotkeys, adjustable noise filtering and a live dictation preview.

This is the public **downloads, documentation and issue-tracking repository**.
Blobscribe is proprietary freeware; its application source is private.

## Download and install

Download **Blobscribe.dmg** and its **.sha256** file from [GitHub Releases](https://github.com/S3bRR/blobscribe-Dictation/releases).

1. Quit any running copy of Blobscribe.
2. Open the DMG and drag Blobscribe into Applications.
3. Open Blobscribe and allow Microphone access when prompted.
4. Allow Blobscribe under System Settings → Privacy & Security → Accessibility
   for automatic text insertion. Reopen the app if macOS asks you to.

Automatic insertion is enabled by default for new installs. Clipboard mode is
available in Settings when you prefer to paste the transcript yourself. Existing
explicit output-mode preferences are respected. The microphone master switch
starts enabled each time the app launches; switch it off in the menu when you
want to stop listening. Push-to-talk captures speech while its shortcut is held.

Requires **Apple Silicon and macOS 14 or later**. The approximately 190 MB English
Whisper model is bundled, so dictation needs no account, API key, subscription or
internet connection. Intel Macs are not included in this release build.

### Signing and first launch

The GitHub app is **ad-hoc signed, not Developer ID signed or notarized**.
Ad-hoc signing verifies local bundle integrity; it does not establish an
Apple-verified publisher identity. macOS may block the first launch. After
trying to open a download you trust, use System Settings → Privacy & Security →
Open Anyway if offered, and confirm. Do not disable Gatekeeper globally.

Verify the download from the folder containing both release files:

```sh
shasum -a 256 -c Blobscribe.dmg.sha256
```

The DMG contains only Blobscribe.app and an Applications shortcut. Keep the
checksum with your download. Existing App Store/sandbox editions may keep their
preferences separately; recheck your shortcuts and output mode when switching
editions. macOS may require Accessibility permission to be enabled again after
replacing an ad-hoc signed app.

## Privacy and permissions

Speech recognition runs locally. There is no account, cloud transcription or
built-in analytics service. Automatic insertion uses macOS Accessibility and
briefly uses the clipboard to paste the transcript. See [PRIVACY.md](PRIVACY.md)
for details, including clipboard-manager behavior.

The GitHub edition uses hardened runtime outside App Sandbox to support its
existing automatic-insertion feature. macOS still controls Microphone and
Accessibility permission. The app does not bypass those permissions.

## Help and feedback

Report reproducible problems in [Issues](https://github.com/S3bRR/blobscribe-Dictation/issues).
Include your macOS version, Mac model, Blobscribe version, output mode and steps
to reproduce. Do not post private recordings, transcripts, passwords or keys.

## License

Blobscribe is free to use under the [Blobscribe Freeware License](LICENSE).
Redistribution, modification and rehosting of the proprietary app require the
copyright holder's permission, subject to applicable law. Share the official
download link instead of uploading copies of the installer.

The Whisper model and bundled open-source libraries retain their own licenses;
see [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt). Their rights are not
restricted by the proprietary application license. This repository does not
contain the private application source.
