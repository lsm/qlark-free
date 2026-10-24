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
   [`qlark-free-3513bfc-2026-10-23.zip` (~611.7 MB)](https://github.com/lsm/qlark-free/releases/download/build-2026-10-23-3513bfc/qlark-free-3513bfc-2026-10-23.zip)
   from the [latest release](https://github.com/lsm/qlark-free/releases/tag/build-2026-10-23-3513bfc).
2. Verify the SHA-256 (`shasum -a 256 <zip>`) matches
   `ceedcc6d86900bb0f347d9731d3fdbe2931c0cc28a41ccbb794a630234568290` — see
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
   Paste unsent. Previously dispatched uncertain text is not automatically pasted
   again. Streaming stops after ten minutes without detected speech.
5. Failed batch recordings appear beside the floating control with Retry and
   Delete (with confirmation). A successful retry saves the text in Saved
   transcripts and shows it for Copy all. Failed, partial or unconfirmed recordings
   may remain locally for recovery.

## This update

- Improved paste confirmation for empty or placeholder inputs and changed caret
  positions; avoids reopening a fully delivered previous session on the next Start.
- Less bookkeeping during long silence, improved hotkey handling, and a message
  instead of a crash when the microphone is unusable.
- Native Liquid Glass transcript bubble on macOS 26+, with a fallback background
  on earlier supported versions.

The program binary matches the version tested by its owner. The download adds
Apple notarization without changing the program or model files. Compatibility
and transcription accuracy in every Mac/input field have not been established.

## Models and licenses

- [Qwen3-ASR 0.6B](https://huggingface.co/Qwen/Qwen3-ASR-0.6B) — MLX 4-bit, Apache-2.0
- [Silero VAD v6.2.1](https://github.com/snakers4/silero-vad/tree/v6.2.1) — MIT

Both ship inside `Qlark.app`. License texts and attribution are in
[Licenses](Licenses) and [THIRD-PARTY.json](THIRD-PARTY.json);
[MODEL-FILES.json](MODEL-FILES.json) records the model hashes, and
[CONTENTS.txt](CONTENTS.txt) lists every file in the download.
