<div align="center">

# 🛡️ MKBVR Pro Ultra
### *(APK-Only Background Stealth & Surveillance Capture Suite)*

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com)
[![Language](https://img.shields.io/badge/Language-100%25_Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![UI Framework](https://img.shields.io/badge/UI-Jetpack_Compose_%2B_3D_Glass-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![Release](https://img.shields.io/badge/Release-v6.0.0_Ultra-FF6F00?style=for-the-badge)](https://github.com/tosprodev/MKBackgroundVideoRecorderApp/releases)
[![Distribution](https://img.shields.io/badge/Distribution-Standalone_APK-crimson?style=for-the-badge)](#%EF%B8%8F-sideloading--manual-installation-apk)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

<p align="center">
  <strong>MKBVR Pro Ultra</strong> is an ultra-premium, production-ready Android surveillance and stealth capture suite distributed exclusively as a standalone APK. Architected with an iOS-inspired 3D glassmorphic design, fluid physics animations, and a modular multi-engine pipeline, MKBVR Pro delivers reliable background recording, on-device AI motion detection, torch-free night vision, hands-free voice control, cryptographic evidence integrity sealing, and per-item Google Drive cloud synchronization.
</p>

[🚀 Key Features](#-key-features--capabilities) •
[🔐 Default PIN](#-default-security-credentials--vault-access) •
[📥 Installation & Play Protect](#%EF%B8%8F-sideloading--manual-installation-apk) •
[🛠️ Tech Stack](#%EF%B8%8F-tech-stack--architecture) •
[📱 Contact](#-developer-profile--contact)

</div>

---

## 🔐 Default Security Credentials & Vault Access

> [!IMPORTANT]
> **First-Time Vault & App Lock Access**
> Upon initial installation and setup, the encrypted media vault and security gate are protected by a default fallback PIN.
>
> * **Default App Password / PIN:** `1234`
> * **Biometric Override:** Fingerprint and Face Unlock (`BiometricPrompt`) can be linked immediately after your first login.
> * **Security Recommendation:** Please navigate to **Settings → Security & Vault Gate** immediately after your first sign-in to update the default PIN (`1234`) to a custom passcode.

---

## 🚀 Key Features & Capabilities

### 🎥 1. 5-Engine Background Capture Suite
MKBVR Pro Ultra operates via five independent, low-overhead foreground/background services designed for uninterrupted capture even when the display is powered off or disguised:

| Capture Engine | Formats & Resolutions | Operational Highlights |
| :--- | :--- | :--- |
| **Background CameraX Video Engine** | `SD`, `HD`, `FHD (1080p)`, `UHD (4K)` (`.mp4`) | Seamless recording in Portrait or Landscape orientations with the screen locked, off, or minimized. |
| **Interval Photo Burst Engine** | High-Res `JPEG` | Automated, scheduled photo bursts captured at customizable millisecond or second intervals. |
| **Background Voice / Audio Engine** | Studio `AAC` (`.m4a`) | Silent background audio capture featuring high-bitrate encoding and live decibel ($\text{dB}$) telemetry. |
| **Background Screen Recorder** | Full-Res `H.264` (`.mp4`) | Captures smooth system display video streams with optional synchronized microphone audio routing. |
| **Interval Screenshot Burst** | Lossless/Crisp `JPEG` | Periodically captures timed display frames directly into the encrypted Vault without cluttering the public gallery. |

---

### 🧠 2. AI Smart Motion Detection & Moving Object AF
* **On-Device Smart Motion Monitoring:** Continuously analyzes raw `YUV_420_888` camera frames on a dedicated background dispatcher thread to identify human silhouettes and moving objects in real time without cloud latency.
* **Non-Destructive Multi-Segment Recording:** Automatically triggers video capture the instant motion enters the frame, initiates a configurable inactivity countdown when movement stops, and cleanly finalizes video segments without leaving zero-byte or corrupted files.
* **Moving Object Auto-Focus (AF):** Dynamically locks continuous autofocus tracking onto active subjects as they traverse the frame for sharp evidentiary capture.

---

### 🌙 3. Camera2 Night Vision *(Pure Sensor Boost — Zero Torch)*
* **Torch-Free Low-Light Enhancement:** Directly interfaces with low-level `Camera2` sensor controls to boost ISO sensitivity gain and extend frame exposure duration in dark environments.
* **100% Covert Operation:** Never triggers the physical LED flashlight, keeping monitoring completely invisible in zero-light conditions.
* **Configurable Hysteresis & Switching Delay:** Uses intelligent luma threshold buffers and adjustable transition timers to prevent rapid ON/OFF flickering in borderline lighting conditions.

---

### 🎙️ 4. Hands-Free Voice AI & Audio Silence Detector
* **Background Speech Recognition:** Continuously listens for low-power custom voice triggers hands-free without requiring physical touch interaction:
  * *"Start monitoring"* — Initializes the active capture profile.
  * *"Stop monitoring"* — Safely finalizes and seals the current session.
  * *"Lock recording"* — Marks the current file as immutable inside the Vault.
* **TTS Voice Confirmations:** Provides spoken Text-to-Speech status confirmations with a dedicated **Silent Stealth Toggle** for total acoustic discretion.
* **Smart Audio Silence Detector:** Monitors ambient sound pressure levels and automatically pauses audio or video recording when noise drops below your custom $\text{dB}$ threshold for a specified duration—instantly resuming the moment sound returns.

---

### 🔒 5. Cryptographic Evidence Mode & Smart Storage
* **Tamper-Evident SHA-256 Seals:** Generates sidecar cryptographic metadata manifests (`.evidence.json`) alongside every recording, binding the file hash with:
  * Exact UTC timestamps
  * Device hardware & sensor fingerprints
  * Optional real-time GPS coordinates
  * `SHA-256` / `HMAC-SHA256` integrity signatures
* **Smart Storage Quota Manager:** Enforces user-defined vault storage limits and automatically rotates/purges the oldest unlocked clips when free disk space approaches the safety reserve threshold.
* **Automated Recording Recovery:** Scans temporary buffers and cache directories on startup to repair and salvage interrupted or unfinalized video segments caused by unexpected battery depletion or forced reboots.

---

### ☁️ 6. Google Drive Cloud Sync & 3D Home Widget
* **Per-Item Cloud Sync Progress:** Uploads encrypted vault media directly to your personal Google Drive or designated Cloud Storage Access Framework (SAF) directory, displaying live percentage progress bars on every gallery card.
* **3D Glassmorphic Home Screen Widget:** Includes an interactive neon home widget providing real-time engine telemetry, storage indicators, and 1-tap stealth capture controls directly from your Android launcher.

---

## 🛠️ Tech Stack & Architecture

| Layer / Component | Technology Implemented |
| :--- | :--- |
| **Core Language** | 100% Kotlin (Strict Null-Safety & Modular Clean Architecture) |
| **UI & Design System** | Jetpack Compose, Material 3, Custom 3D Glassmorphism AGSL/Canvas Shaders |
| **Camera Pipeline** | Android Jetpack `CameraX` (`Core`, `VideoCapture`, `ImageAnalysis`) + `Camera2` Interop |
| **Asynchronous Concurrency** | Kotlin Coroutines, Structured Concurrency & Reactive `StateFlow` / `SharedFlow` |
| **Background Execution** | Android Foreground Services, WakeLocks, `MediaProjection` & Hardware Encoder Pipelines |
| **Security & Cryptography** | `BiometricPrompt` (Class 3 Biometrics), Device Credential Fallback, `SHA-256` / `HMAC-SHA256` |
| **Cloud & Storage** | Google Drive API / Android Storage Access Framework (SAF) & Scoped Vault Storage |

---

## 📥 Sideloading & Manual Installation (APK)

> [!WARNING]
> **Why This App Is Not on Google Play Store (Play Protect Notice)**
> Because **MKBVR Pro Ultra** includes unrestricted background camera, microphone, screen capture, and persistent stealth services that exceed standard Google Play Store policies, it is distributed **exclusively as an independent standalone APK**.
>
> Consequently, **Google Play Protect** may display an *"Unrecognized App"* or *"Harmful App Blocked"* warning during installation. **You must disable Google Play Protect prior to installing the APK** to prevent Android from blocking the installation or restricting background services.

### Step 1: Disable Google Play Protect (Required Before Installation)
1. Open the **Google Play Store** app on your Android device.
2. Tap your **Profile Icon** in the top-right corner.
3. Select **Play Protect** from the menu, then tap the **Settings (Gear ⚙️)** icon in the top-right corner.
4. Toggle **OFF** *"Scan apps with Play Protect"* (and *"Improve harmful app detection"*).
5. Confirm by tapping **Turn off**.

### Step 2: Sideload the APK Package
1. **Download:** Grab the latest `MKBVR_Pro_v6.0.0_Release.apk` package from the [Releases](https://github.com/tosprodev/MKBackgroundVideoRecorderApp/releases) page directly onto your Android device.
2. **Launch Installer:** Open your device's **File Manager** and tap on `MKBVR_Pro_v6.0.0_Release.apk`.
3. **Allow Unknown Sources:** If prompted by Android security or your package installer, enable **"Allow from this source"** (Install Unknown Apps) for your browser or file manager.
4. **Install & Initialize:** Complete the installation and launch **MKBVR Pro Ultra**.

### Step 3: Initial Setup & Permissions Gate
1. Enter the default security PIN (`1234`) when prompted at the initial Vault lock screen.
2. Grant the required runtime permissions during the onboarding security gate:
   * 📷 **Camera** *(Required for Background Video, Photo Burst & Night Vision)*
   * 🎙️ **Microphone** *(Required for Studio Audio, Video Audio & Voice AI Triggers)*
   * 🔔 **Notifications** *(Required for Foreground Service persistence on Android 13+)*
   * 📍 **Location (Optional)** *(Used only if GPS stamping is enabled in Cryptographic Evidence Mode)*
3. *(Optional but Recommended)* Disable **Battery Optimization** (Set to *Unrestricted*) for MKBVR Pro Ultra in your Android App Info settings to prevent OEM battery killers from interrupting long background recording sessions.

---

## 📱 Developer Profile & Contact

Need custom enterprise builds, architectural consultation, or bug support? Reach out directly to the lead developer:

* **Lead Architect & Developer:** Md Kaif
* **GitHub Repository:** [tosprodev/MKBackgroundVideoRecorderApp](https://github.com/tosprodev/MKBackgroundVideoRecorderApp)
* **Developer Profile:** [@tosprodev](https://github.com/tosprodev)
* **Direct Phone / WhatsApp:** [`+91 6003690840`](tel:+916003690840)
* **Official Email:** [kaif.mth@gmail.com](mailto:kaif.mth@gmail.com)

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file in this repository for full license text and permissions.

<div align="center">
  <sub>Built with ❤️ and Kotlin by <strong>Md Kaif (@tosprodev)</strong></sub>
</div>
