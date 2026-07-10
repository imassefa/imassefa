Hi there!! 👩🏽‍💻

I'm a Computer Engineering & Computer Science student (EE + CS) at USC Viterbi. I like working close to the hardware, where software decisions directly affect physical and human centered systems.

Right now I'm working on robotics software and hardware, with the goal of deploying more robotics into the world and helping other people deploy faster.

What I'm into 😁❤️‍🔥


Robot learning and physical data infrastructure 🤖
Brain computer interfaces, noninvasive & invasive 🧠
Robotics and assistive technology
Embedded systems and hardware/software integration


Almaz ⚡ (active, in progress)

Multimodal physical data grounding layer for robotics. Ingests synchronized video, force-torque, proprioception, and spatial-awareness streams from robot manipulation episodes, aligns them on a common timeline, runs inference, and emits structured per-frame labels: phase, contact, grasp quality, task progress, failure flags.

Backend. FastAPI + Celery + Redis + PostgreSQL + S3/MinIO, containerized with Docker. Async multimodal processing built on VideoMAE and SAM.

ML pipeline. A PELT heuristic segmenter handles manipulation phase detection (reach, grasp, lift, place, idle), feeding a dilated temporal convolutional network trained on pseudo-labels. A 16-feature physics extractor derives a contact proxy from gripper velocity and Z-deceleration, over Butterworth-filtered force-torque signals.

Cross-embodiment data. Streaming OXE loader across DROID, ALOHA, and UMI (LeRobot / HuggingFace format), a leave-one-embodiment-out benchmark harness, and LeRobot-compatible Parquet export.

Frontend. React + Vite + TypeScript. Video player with phase timeline overlay, grasp quality card, and a human label-correction UI.

Almaz started as neuroadaptive robotics: training robot behavior from EEG signals, using MNE-Python for neural signal processing and Webots for simulated embodiments. It moved toward physical data grounding in June 2026.

Other things I've built ⚙️

ÆON HUD. Real-time biometric HUD overlay for macOS. Python + MediaPipe + OpenCV + PyQt6. Tracks a 478-landmark face mesh and iris gaze through the built-in camera and renders a transparent overlay across the screen. Per-eye blink and wink detection via the Eye Aspect Ratio algorithm drives a gesture state machine (left wink selects, right wink pastes, a double blink within 0.8s executes), wired to real macOS Accessibility API actions. Iris landmarks drive a four-quadrant gaze ray. Multi-layer OpenCV compositor with per-layer alpha blending, and a daemon-thread camera pipeline with a frame-drop queue so the display never lags the capture.

AVR Embedded Speed Trap. embedded-speed-trap · C on AVR. Measures object speed between two LED/phototransistor gates using hardware timers, computing speed with scaled integer arithmetic rather than floating point. Drives an LCD readout and a servo speed dial, with user-set high/low thresholds persisted in EEPROM and RGB LED feedback classifying each pass. Raw ADC samples are normalized through a calibrated linear mapping.

drift. iOS app for practicing difficult conversations and assertiveness. React Native (Expo, bare workflow) + TypeScript. 990 lessons, 270 hand-curated and 720 generated with Claude Opus using structured outputs. Ollie the otter mascot runs on a wellbeing decay model that feeds on daily practice. RevenueCat paywall with a 7-day trial. Submitted to the App Store.

GetOut (in progress). Location-based daily dare app that pushes you to explore your city. React Native (Expo Router) + Supabase. Vision-board aesthetic: oversized two-tone type, full-bleed saturated fields. Supabase backend with a demo mode that falls back to Zustand + AsyncStorage when env vars are blank. Map layer on react-native-maps with a 15-mile radius, emoji spot markers, and heat blobs over a custom Google Maps style.

Magic Hands. Real-time hand gesture recognition with a cyberpunk overlay. Python + MediaPipe Tasks + OpenCV. 21 landmarks per hand rendered as a full skeleton graph, with per-fingertip motion trails and glow-line compositing: a soft wide halo layer under a crisp 1px base.

Letterpose. Keyboard-driven GTM outreach tool. Next.js + Supabase + Resend on Vercel. HTML email composer with a floating link toolbar and a {placeholder} system, behind a full shortcut layer: ⌘↵ to send, ⌘K search palette, j/k nav, C to cycle contacts.

I also run two scheduled Claude agents on GitHub Actions that summarize robotics/AI news and market activity into daily push briefs.

Tools

Systems & embedded. C, AVR/ATmega, register-level programming, ADCs, hardware timers, interrupts, PWM, EEPROM, servo control

ML & perception. PyTorch, VideoMAE, SAM, MediaPipe, OpenCV, MNE-Python, LeRobot, temporal convolutional networks

Backend. Python, FastAPI, Celery, Redis, PostgreSQL, Docker, S3/MinIO, Supabase

Frontend. TypeScript, React, Vite, Next.js, React Native / Expo

Always up for talking about neurotech, robot learning, assistive robotics, and anything that blinks an LED for a good reason.
