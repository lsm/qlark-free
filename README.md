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
   [`qlark-free-996b010-2026-11-06.zip` (~611.8 MB)](https://github.com/lsm/qlark-free/releases/download/build-2026-11-06-996b010/qlark-free-996b010-2026-11-06.zip)
   from the [latest release](https://github.com/lsm/qlark-free/releases/tag/build-2026-11-06-996b010).
2. Verify the SHA-256 (`shasum -a 256 <zip>`) matches
   `f7a7f6766dc2ad0bfd77315ec0699cb77ef99577c22eb40122201d4790fdb472` — see
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
   again. Turn on **Don't show sent pastes in bubble** in the menu to treat text
   Qlark sent as delivered, for apps that can't confirm a paste. Streaming stops
   after ten minutes without detected speech.
5. Failed batch recordings appear beside the floating control with Retry and
   Delete (with confirmation). A successful retry saves the text in Saved
   transcripts and shows it for Copy all. Failed, partial or unconfirmed recordings
   may remain locally for recovery.

## This update

- New menu option **Don't show sent pastes in bubble** (off by default) keeps text
  Qlark sent out of the bubble when the target app can't confirm the paste.
- **Check for speech** (on by default) skips batch recordings that contain no
  speech and trims silence at the edges.
- Streaming text confirmed as pasted is no longer saved to disk; unsent, uncertain
  and partial text still is. Turn on **Save all transcripts** to keep everything.
- Each Streaming session's files are deleted once its text is confirmed, closed
  or replaced.

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
