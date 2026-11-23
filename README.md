# TMR Cue Studio

A static, GitHub Pages-compatible keyword-to-audio sequence builder.

## Features
- Browser text-to-speech for each keyword
- Locally generated continuous white noise during the sequence
- Configurable 1.0–2.0 second cue slots
- Configurable 4.0–5.0 second gaps
- Fixed cue/gap timing regardless of keyword count
- Speech rate and relative output controls
- JSON export of the cue plan
- No backend, account, API key, or external dependency

## Deploy on GitHub Pages
1. Create or open a GitHub repository.
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select your main branch and `/ (root)`, then save.
6. Open the Pages URL GitHub provides.

## Important audio limitations
- Browser speech synthesis uses voices supplied by the device/browser. Voice availability, pronunciation, and latency vary.
- The selected cue slot is fixed. Speech that exceeds the slot is stopped at its boundary; short words may finish before the slot ends.
- The gap is measured after the fixed cue slot. White noise continues during cue slots and gaps.
- The percentage controls are digital output levels, not calibrated sound-pressure levels (dB SPL). Actual ear-level SPL depends on device output, system volume, transducer/headphone sensitivity, fit, and measurement conditions.
- This app does not certify or guarantee the requested dB SPL thresholds. Verify levels with appropriate calibrated equipment and qualified adult/research-supervisor oversight before any participant testing.
- This browser implementation is intended for development and controlled, supervised testing while participants are awake. Do not use it for unattended overnight playback.
- Browser TTS audio is not exported as a WAV file by this version. The JSON export saves the cue plan and settings only.

## Browser
Use a current browser with Web Speech API and Web Audio API support. Chrome-based browsers generally provide the broadest support, but available voices are device-dependent.
