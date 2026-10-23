# Qlark Free

Fully offline voice input for macOS. Press a hotkey, speak, and the text lands in
whatever you are typing into — transcription runs entirely on your Mac, with the
speech models bundled inside the app.

![Audio flows from the microphone through on-device transcription to text output](assets/flow.svg)

For macOS users on **Apple Silicon (macOS 15.0 or newer)** who want dictation
with no cloud service, no account, and no model downloads. The app is
Apple-notarized.

## Get it

1. Download
   [`qlark-free-e26a72d-2026-10-22.zip` (~611.7 MB)](https://github.com/lsm/qlark-free/releases/download/build-2026-10-22-e26a72d/qlark-free-e26a72d-2026-10-22.zip)
   from the [latest release](https://github.com/lsm/qlark-free/releases/tag/build-2026-10-22-e26a72d).
2. Verify the SHA-256 (`shasum -a 256 <zip>`) matches
   `b2e4092482c8e44da59fae6c9dc72ab4af34b21c30b4e703e8052e7bee321fbd` — see
   [SHA256SUMS](SHA256SUMS).
3. Unzip and drag `Qlark.app` into Applications. The ASR and VAD models are
   already inside the app; download the release ZIP, not GitHub's auto-generated
   "Source code" archives, which do not contain the app.

**解压后只需把 Qlark.app 拖进 Applications；模型已内置。**

## Use it

1. Open Qlark and grant Microphone and Accessibility access when prompted
   (System Settings → Privacy & Security → Accessibility).
2. Qlark lives in the menu bar with a floating control and no Dock icon.
   **Option-Space** or the floating button starts and stops dictation.
3. Focus an editable field and speak. Batch mode transcribes when you stop
   (five-minute recording limit); optional **Streaming** transcribes at pauses
   while recording continues.
4. Unsent or unconfirmed text stays in a fallback bubble with Copy all and
   Paste unsent; failed or partial recordings may remain locally for recovery.

## Models and licenses

- [Qwen3-ASR 0.6B](https://huggingface.co/Qwen/Qwen3-ASR-0.6B) — MLX 4-bit, Apache-2.0
- [Silero VAD v6.2.1](https://github.com/snakers4/silero-vad/tree/v6.2.1) — MIT

Both ship inside `Qlark.app`. License texts and attribution are in
[Licenses](Licenses) and [THIRD-PARTY.json](THIRD-PARTY.json);
[CONTENTS.txt](CONTENTS.txt) lists every file in the download.
