# User Stories & Behaviors

1. **Easy install (macOS & Windows)**
   - Clone repo, install Node + Python deps once; packaged app will ship as a single installer for one-click launch.

2. **One-click start/stop**
   - From the desktop app, press a single button to start live transcription; backend boots automatically.

3. **Choose save path (v1)**
   - On first launch, user picks the folder where transcripts are stored; path can be changed later in Settings.

4. **Audio source selection**
   - User can choose microphone, system audio, or both. Example: join a Zoom meeting and transcribe system + mic.

5. **Language selection**
   - Choose English, Spanish, or bilingual mode before starting a session.

6. **Resilience on shutdown**
   - If the computer powers off unexpectedly, in-progress transcript is saved up to the last received chunk.

7. **App close safety**
   - Closing the app while recording saves the latest transcript snapshot automatically.

8. **Custom save folder & formats**
   - User selects a folder; all transcripts are stored there as plain `.txt` and optionally `.pdf` exports.

8. **Live subtitles widget**
   - Optional floating widget displays live transcript for any active source (system or mic); toggle on/off from main app.

9. **Main app toggles**
   - Global switch in the app enables/disables live transcription and the widget without closing the app.

10. **LLM summary on demand (v2)**
    - Using the user’s preferred LLM (e.g., Claude via API key), generate a summary of the current transcript.

11. **Live Q&A with AI (v2)**
    - During an active session, ask questions about what’s being transcribed and get AI answers in real time.

12. **Knowledge export (v2)**
    - Summarize all stored transcripts and export for fine-tuning or personal agent training (local file output, no remote DB).

13. **Widget appearance (v2)**
    - User can set widget font size and colors for readability.

## Notes
- Backend: FastAPI; Frontend: Electron. Monolithic app bundles both for offline use.
