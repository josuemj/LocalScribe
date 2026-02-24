# Overview
LocalScribe is a local-first desktop app (macOS/Windows) that live-transcribes English and Spanish from microphone and/or system audio. It’s handy for multilingual calls, classes, and meetings, and can feed saved transcripts into local AI workflows for summaries or training—no paid cloud memberships required, fully open source.

## Example Use Cases
- Students capturing free transcripts from Zoom classes without sending audio to the cloud.
- Professionals saving important video-conference transcripts (system + mic) for meeting minutes.
- Language learners following bilingual conversations with live subtitles.
- Researchers journaling interviews and exporting clean text/PDF for analysis.
- Creators grabbing quick subtitles from screen recordings or demos.

# User Stories & Behaviors

## MVP
1. **Easy install (macOS & Windows)** — Clone repo, install Node + Python deps once; packaged app will ship as a single installer for one-click launch.
2. **One-click start/stop** — Single button starts/stops live transcription; backend boots automatically.
3. **Choose save path (v1)** — On first launch, pick folder for transcripts; changeable later in Settings.
4. **Audio source selection** — Choose microphone, system audio, or both (e.g., Zoom meeting capture).
5. **Language selection** — Choose English, Spanish, or bilingual mode before starting a session.
6. **Resilience on shutdown** — If the computer powers off, transcript is saved up to the last received chunk.
7. **App close safety** — Closing the app while recording saves the latest transcript snapshot automatically.
8. **Custom save folder & formats** — Store transcripts as `.txt` and optionally `.pdf` exports in the chosen folder.
9. **Live subtitles widget** — Optional floating widget showing live transcript for any active source; toggle on/off.
10. **Main app toggles** — Global switch to enable/disable live transcription and the widget without closing the app.
11. **Audio device picker** — List input/output devices with a live level meter to confirm capture.
12. **Hotkeys** — Global shortcuts to start/stop transcription and toggle the widget without focusing the app.
13. **Localization (EN/ES UI)** — App UI available in English and Spanish to match transcript language choice.

## Future (v2+)
1. **LLM summary on demand** — Use user-provided LLM key (e.g., Claude) to summarize the current transcript.
2. **Live Q&A with AI** — Ask questions during an active session and get real-time answers from the transcript.
3. **Knowledge export** — Summarize all stored transcripts and export for fine-tuning or personal agent training (local files only).
4. **Widget appearance** — Customize widget font size and colors for readability.
5. **Session management** — Name/rename sessions, add tags, and filter/search by date, language, or tag.

## Notes
- Backend: FastAPI; Frontend: Electron. Monolithic app bundles both for offline use.
