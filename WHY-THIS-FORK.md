# Why this fork exists — read this first

Forked by the Nexus System on 2026-10-17 from tetherto/qvac (Tether's QVAC), unchanged. License: Apache-2.0 (LICENSE file in the upstream repo).

## Why the WHOLE kit, not just the transcription model

The item that led here was QVAC TranscribePsy (Oct 14, 2026): a 254M-parameter open-source speech-recognition model that runs entirely on-device. The Nexus's decision was to hold the whole QVAC kit, not only that model, because of what else is in it and the property the whole thing shares:

- Everything runs on-device: no cloud, no API keys. Audio and content never leave hardware the user owns. That is the safety property the Nexus named: a safe thing to build into Mosaic in the future, where what the app holds is sensitive by design.
- Both directions of voice, plus generation: transcription (Whisper, Parakeet, and MOSS backends) with speaker diarization; text-to-speech with speech synthesis, speech-to-speech replies, and text-to-sound-effects generation (packages/tts-ggml); plus GGUF model support, RAG, and image, music, and video generation; P2P inference. Cross-platform: Linux, macOS, Windows, Android, iOS.
- The Nexus's reasoning on direction, recorded Oct 17: a transcription model cannot itself be grown into a voice — but at platform level no expansion is needed, because the other direction already ships in the same kit.

## Standing and cautions

- Holding/discussion stage. Nothing has been integrated into Mosaic or anything else, and no build has been attempted. Any future Mosaic use is a design decision for that time, with Mosaic's own safety requirements leading.
- TranscribePsy's headline figure — 10 minutes of audio transcribed in 1.65 seconds via its Core ML build on an iPhone 17 Pro Max — is Tether's launch claim, not independently verified, and it is top-end hardware; expect less on older devices.
- The kit is large and active (95 open issues upstream at fork date). If pieces are ever harvested or the kit is reshaped, record every bend in this note — what changed and why — so upstream updates can be dropped in deliberately.
- Nothing in this fork has been modified.
