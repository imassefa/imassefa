# Hi there!! 👩🏽‍💻👩🏽‍💻

I'm a Computer Engineering & Computer Science student (EE + CS) at USC Viterbi. I like working close to the hardware, where software decisions directly affect physical and human centered systems.

> Right now I'm working on robotics software and hardware, with the goal of deploying more robotics into the world and helping other people deploy faster.

### What I'm into 😁❤️‍🔥

- 🤖 &nbsp;Robot learning and physical data infrastructure
- 🧠 &nbsp;Brain computer interfaces, noninvasive & invasive
- 🦾 &nbsp;Robotics and assistive technology
- ⚙️ &nbsp;Embedded systems and hardware/software integration

<br>

## ⚡ Almaz

*Active, in progress*

**A multimodal physical data grounding layer for robotics.**

Ingests synchronized video, force-torque, proprioception, and spatial-awareness streams from robot manipulation episodes. Aligns them on a common timeline, runs inference, and emits structured per-frame labels: phase, contact, grasp quality, task progress, failure flags.

**ML pipeline**
- PELT heuristic segmenter for manipulation phase detection (reach, grasp, lift, place, idle)
- Dilated temporal convolutional network trained on pseudo-labels
- 16-feature physics extractor deriving a contact proxy from gripper velocity and Z-deceleration, over Butterworth-filtered force-torque signals

**Cross-embodiment data**
- Streaming OXE loader across DROID, ALOHA, and UMI (LeRobot / HuggingFace format)
- Leave-one-embodiment-out benchmark harness
- LeRobot-compatible Parquet export

**Systems**
- `FastAPI` `Celery` `Redis` `PostgreSQL` `S3/MinIO` `Docker`, with async multimodal processing on VideoMAE and SAM
- `React` `Vite` `TypeScript` frontend: video player with phase timeline overlay, grasp quality card, human label-correction UI

Almaz started as neuroadaptive robotics: training robot behavior from EEG signals, using MNE-Python for neural signal processing and Webots for simulated embodiments. It moved toward physical data grounding in June 2026.

<br>

## ⚙️ Other things I've built

### ÆON HUD
*Real-time biometric HUD overlay for macOS.* &nbsp; `Python` `MediaPipe` `OpenCV` `PyQt6`

- Tracks a 478-landmark face mesh and iris gaze through the built-in camera, rendering a transparent overlay across the screen
- Per-eye blink and wink detection via the Eye Aspect Ratio algorithm
- Gesture state machine wired to real macOS Accessibility API actions: left wink selects, right wink pastes, a double blink within 0.8s executes
- Iris landmarks drive a four-quadrant gaze ray
- Multi-layer OpenCV compositor with per-layer alpha blending
- Daemon-thread camera pipeline with a frame-drop queue, so the display never lags the capture

### AVR Embedded Speed Trap
*Measures object speed between two optical gates.* &nbsp; `C` `AVR` &nbsp; [`embedded-speed-trap`](https://github.com/imassefa/embedded-speed-trap)

- Times objects across dual LED/phototransistor gates using hardware timers
- Computes speed with scaled integer arithmetic rather than floating point
- Drives an LCD readout and a servo speed dial
- User-set high/low thresholds persisted in EEPROM, with RGB LED feedback classifying each pass
- Raw ADC samples normalized through a calibrated linear mapping

### drift
*iOS app for practicing difficult conversations and assertiveness.* &nbsp; `React Native` `Expo` `TypeScript`

- 990 lessons: 270 hand-curated, 720 generated with Claude Opus using structured outputs
- Ollie the otter mascot runs on a wellbeing decay model that feeds on daily practice
- RevenueCat paywall with a 7-day trial
- Submitted to the App Store

### GetOut
*Location-based daily dare app that pushes you to explore your city.* &nbsp; `React Native` `Expo Router` `Supabase` &nbsp; *(in progress)*

- Vision-board aesthetic: oversized two-tone type, full-bleed saturated fields
- Supabase backend with a demo mode that falls back to Zustand + AsyncStorage when env vars are blank
- Map layer on react-native-maps: 15-mile radius, emoji spot markers, heat blobs over a custom Google Maps style

### Magic Hands
*Real-time hand gesture recognition with a cyberpunk overlay.* &nbsp; `Python` `MediaPipe Tasks` `OpenCV`

- 21 landmarks per hand rendered as a full skeleton graph
- Per-fingertip motion trails with alpha-faded history
- Glow-line compositing: a soft wide halo layer under a crisp 1px base

### Letterpose
*Keyboard-driven GTM outreach tool.* &nbsp; `Next.js` `Supabase` `Resend` `Vercel`

- HTML email composer with a floating link toolbar and a `{placeholder}` system
- Full shortcut layer: `⌘↵` send, `⌘K` search palette, `j`/`k` nav, `C` cycle contacts

I also run two scheduled Claude agents on GitHub Actions that summarize robotics/AI news and market activity into daily push briefs.

<br>

## 🧰 Tools

| | |
|---|---|
| **Systems & embedded** | C, AVR/ATmega, register-level programming, ADCs, hardware timers, interrupts, PWM, EEPROM, servo control |
| **ML & perception** | PyTorch, VideoMAE, SAM, MediaPipe, OpenCV, MNE-Python, LeRobot, temporal convolutional networks |
| **Backend** | Python, FastAPI, Celery, Redis, PostgreSQL, Docker, S3/MinIO, Supabase |
| **Frontend** | TypeScript, React, Vite, Next.js, React Native / Expo |

<br>

Always up for talking about neurotech, robot learning, assistive robotics, and anything that blinks an LED for a good reason.
