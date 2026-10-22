# Qlark Free

A floating, on-device dictation app for Apple Silicon Macs.

## Download / 下载

[**Download Qlark — 611.7 MB**](https://github.com/lsm/qlark-free/releases/download/build-2026-10-22-e26a72d/qlark-free-e26a72d-2026-10-22.zip)

[Release notes and checksum](https://github.com/lsm/qlark-free/releases/tag/build-2026-10-22-e26a72d)

**Apple Silicon only · macOS 15.0 or newer.** Unzip and drag only `Qlark.app` into
Applications. The ASR and VAD models are already inside the app: **no separate
model folder or model download is needed**. Transcription runs on this Mac.
GitHub's automatic “Source code” archives do not contain the app or models.

**解压后只需把 Qlark.app 拖进 Applications。模型已内置，不用另拷模型或下载。**

## Install and use / 安装和使用

1. Quit older copies, unzip the download, then replace `/Applications/Qlark.app`.
2. Open Qlark and confirm the normal first-open dialog if shown.
3. Grant Microphone and Accessibility when requested. If needed, enable the app
   in System Settings → Privacy & Security → Accessibility.
4. Wait for Ready. Qlark lives in the menu bar and floating control, without a
   Dock icon. Use **Option-Space** or the floating button to start and stop.
5. Focus an editable field to receive dictation. Confirmed delivery is quiet;
   if **Paste sent — check the target** appears, check the target before pasting
   again to avoid a duplicate.

Batch mode transcribes when you stop, with a five-minute recording limit and an
elapsed-time display. Optional **Streaming** is in the lark's menu: it transcribes
at pauses while recording continues. The fallback transcript bubble retains
unsent or unconfirmed text; it has a seven-line scroll area, Copy all, Paste
unsent and Close. Already-dispatched uncertain text is not automatically replayed.
Saved transcripts are available from the menu. Failed, partial or unconfirmed
recordings may remain locally for recovery; closing the bubble does not erase them.

## This build / 本版

- Release lean build from source commit `e26a72d63c288c11296b528142fe396b4af271d4`.
- The owner installed and opened this exact Release build, then accepted the
  Liquid Glass bubble appearance. This is not a comprehensive compatibility or
  transcription-accuracy test across other Macs/apps.
- Native Liquid Glass bubble on **macOS 26+**; earlier supported macOS versions
  retain the existing background. The bird animation and seven-bar meter remain.
- Includes the empty-paragraph first-paste confirmation change, retained-history
  scan performance fix and quiet confirmed delivery.
- **Apple-notarized / 已通过 Apple 公证。**
- ZIP: **611,696,057 bytes** (611.7 MB / 583.4 MiB). Check
  [SHA256SUMS](SHA256SUMS) before installing.

See [CONTENTS.txt](CONTENTS.txt) for every ZIP entry. The repository distributes
binaries, model files and attribution; it does not publish the private app source
or its Git history. No recordings, transcripts, Sessions, credentials or local
user paths are included in the download.

## Models and licenses / 模型和许可

Both models and their full license/attribution files are inside
`Qlark.app/Contents/Resources/`. Copies of the notices are in [Licenses](Licenses).

- **Qwen3-ASR 0.6B, MLX 4-bit** — Apache-2.0. Original
  [Qwen / Alibaba Cloud](https://huggingface.co/Qwen/Qwen3-ASR-0.6B),
  [MLX conversion by aufklarer](https://huggingface.co/aufklarer/Qwen3-ASR-0.6B-MLX-4bit).
  See [LICENSE](Licenses/Qwen3-ASR-LICENSE.txt) and the distribution-authored
  [NOTICE](Licenses/Qwen3-ASR-NOTICE.txt).
- **Silero VAD v6.2.1, MLX** — MIT. [Silero Team](https://github.com/snakers4/silero-vad/tree/v6.2.1),
  [aufklarer conversion](https://huggingface.co/aufklarer/Silero-VAD-v6.2.1-MLX/tree/0046cea48b26401909b24292b688fbc9b6322bc5).
  Pinned revision `0046cea48b26401909b24292b688fbc9b6322bc5`.
  See [LICENSE](Licenses/Silero-VAD-LICENSE.txt) and
  [NOTICE](Licenses/Silero-VAD-NOTICE.txt).

No forced-alignment model or alignment worker is bundled. Software dependencies
use Apache-2.0, MIT, and the Swift runtime's Apache-2.0 with Runtime Library
Exception. Full texts and component versions are listed in
[Licenses](Licenses) and [THIRD-PARTY.json](THIRD-PARTY.json).
