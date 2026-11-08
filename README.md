MKBVR Pro Ultra (APK-Only Background Stealth Suite)
MKBVR Pro Ultra is an ultra-premium, production-ready Android surveillance and stealth capture suite distributed as a standalone APK. Architected with iOS-inspired 3D glassmorphic design, fluid animations, and a modular multi-engine pipeline, MKBVR Pro provides secure background recording, AI motion detection, torch-free night vision, hands-free voice control, cryptographic evidence integrity sealing, and per-item Google Drive cloud synchronization.

🚀 Key Features & Capabilities
5-Engine Background Capture Suite

Background CameraX Video Engine: Records high-resolution video (SD, HD, FHD, UHD) in portrait or landscape while the screen is off or disguised.

Interval Photo Burst Engine: Automatically captures scheduled high-res JPEG photo bursts at custom intervals.

Background Voice / Audio Recorder: Records high-bitrate studio AAC (.m4a) audio silently in the background with real-time decibel tracking.

Background Screen Recorder: Records full-screen H.264 video streams with optional microphone audio.

Interval Screenshot Burst: Automatically captures crisp timed JPEG screenshots of the device display directly into the Vault.

AI Smart Motion Detection & Moving Object AF

Smart Motion Monitoring: Analyzes YUV_420_888 camera frames on-device in a background thread to detect human silhouettes or general moving objects.

Non-Destructive Multi-Segment Recording: Automatically starts recording segments only when motion is detected, runs an inactivity countdown when movement stops, and finalizes segments cleanly without creating empty files.

Moving Object Auto-Focus: Dynamically locks continuous autofocus tracking onto active subjects as they move across the frame.

Camera2 Night Vision (Pure Sensor Boost — Zero Torch)

Torch-Free Low-Light Enhancement: Boosts Camera2 sensor ISO gain and frame exposure duration in dark environments without ever activating the visible LED flashlight, keeping monitoring completely covert.

Configurable Hysteresis & Delay: Prevents rapid ON/OFF flickering using luma thresholds and adjustable switching delays.

Hands-Free Voice AI & Audio Silence Detector

Background Speech Recognition: Continuously listens for custom voice triggers ("start monitoring", "stop monitoring", "lock recording") hands-free without button presses.

TTS Voice Confirmations: Automatically speaks confirmation replies (with an option to mute for complete silence).

Audio Silence Detector: Automatically pauses audio or video recording when ambient noise stays below your dB threshold for a specified timeout, instantly resuming the moment sound returns.

Cryptographic Evidence Mode & Smart Storage

Tamper-Evident SHA-256 Seals: Generates cryptographic metadata manifests (.evidence.json) containing UTC timestamps, device hardware fingerprints, and optional GPS coordinates.

Smart Storage Manager: Automatically enforces maximum vault quotas and cleans up oldest clips when disk space reaches the safety reserve threshold.

Recording Recovery: Scans cache and temporary directories to repair and restore interrupted or unfinalized video segments.

Google Drive Cloud Sync & 3D Home Widget

Per-Item Cloud Progress: Syncs vault recordings directly to your personal Google Drive or Cloud SAF folder with real-time percentage progress tracking on each item in the gallery.

3D Glassmorphic Home Widget: Provides an interactive neon widget displaying live engine telemetry and 1-tap capture controls directly on your home screen.

🛠️ Tech Stack & Architecture
Language: 100% Kotlin

UI Framework: Jetpack Compose with Material 3 & Custom 3D Glassmorphism Shaders

Camera Architecture: CameraX Core, VideoCapture, ImageAnalysis, and Camera2 Interop

Concurrency: Kotlin Coroutines & Flow (StateFlow)

Security: BiometricPrompt (Fingerprint/Face), Android Device Credential Fallback, SHA-256 / HMAC-SHA256 Cryptographic Sealing

📥 Sideloading & Manual Installation (APK)
Because this distribution is provided as a pre-compiled APK package for manual sideloading:

Download the latest MKBVR_Pro_v6.0.0_Release.apk file directly to your Android device.

Open your file manager and tap the APK file.

When prompted by Android security or your device package installer, allow installation from Unknown Sources for your browser or file manager.

Complete the installation, open the app, and grant the required Camera, Microphone, and Notification permissions during the initial security startup gate.

📱 Developer Profile & Contact
Lead Architect & Developer: Md Kaif

GitHub Repository: tosprodev/MKBackgroundVideoRecorderApp

Developer Profile: github.com/tosprodev

Direct Phone: +916003690840

Official Email: kaif.mth@gmail.com

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.