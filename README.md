<div align="center">

  <img src="app/src/main/res/drawable/ic_app_logo.xml" alt="SIP Dialer Pro Logo" width="110" height="110" />

  <h1>📞 SIP Dialer Pro</h1>

  <p>
    <strong>A lightweight, modern, and feature-rich Android VoIP & SIP Client powered by Linphone SDK.</strong>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Platform-Android%207.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android" />
    <img src="https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
    <img src="https://img.shields.io/badge/VoIP%20Engine-Linphone%20SDK%205.2-FF6F00?style=for-the-badge" alt="Linphone SDK" />
    <img src="https://img.shields.io/badge/Build-GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions" />
  </p>

</div>

---

## ✨ Key Features

- 🔐 **Persistent SIP Auto-Login:** Supports **UDP**, **TCP**, and **TLS** transports. Saves credentials locally so you stay connected automatically on launch.
- 🎨 **Modern Gradient UI & Circular Dialpad:** Sleek dark-teal gradient interface with haptic-feedback dialpad keys and live DTMF tone support.
- 📊 **Real-Time Call Quality Analytics:** Displays a detailed post-call quality popup featuring **MOS Score (1.0 – 5.0)**, **Packet Loss (%)**, **Jitter Buffer (ms)**, **Latency (ms)**, and **Audio Codec**.
- ⏺️ **Built-In Call Recording:** One-tap call recording saved directly as high-clarity `.wav` files in `Android/data/com.sip.dialer/files/Recordings/`.
- ⏱️ **Live In-Call Controls & Timer:** Real-time call duration counter (`MM:SS`) along with **Mute**, **Speakerphone**, and **End Call** controls.
- 🕒 **Recent Call History:** Tracks Outgoing (`📤`), Incoming (`📥`), and Missed (`❌`) calls with timestamps and durations—tap any entry to redial instantly.
- 📇 **Native Contacts Integration:** Seamlessly pick and dial phone numbers directly from your Android device contacts.
- 📱 **Smart Proximity Sensor:** Automatically turns off the screen when the phone is held near your ear during active calls.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Kotlin (JVM 17) |
| **VoIP / SIP Core** | `org.linphone:linphone-sdk-android:5.2.98` |
| **UI & Layout** | Android XML, Material Components, Vector Drawables |
| **CI / CD Pipeline** | GitHub Actions (`gradle assembleDebug`) |
| **Min / Target SDK** | API 24 (Android 7.0) / API 34 (Android 14+) |

---

## 🚀 Automated APK Build (GitHub Actions)

This repository is configured with **GitHub Actions** to compile the Android APK automatically in the cloud—no local Android Studio setup required:

1. Push any code changes to the `main` branch.
2. Navigate to the **Actions** tab in this repository.
3. Open the latest **Build Android APK** workflow run.
4. Download **`BasicSipDialer-APK`** from the **Artifacts** section and install `app-debug.apk` on your Android device.

---

## 📁 Project Structure

```text
BasicSIP/
├── .github/workflows/
│   └── build-apk.yml              # Automated cloud APK build workflow
├── app/
│   ├── build.gradle               # App dependencies & Linphone SDK config
│   └── src/main/
│       ├── AndroidManifest.xml    # Permissions & app metadata
│       ├── java/com/sip/dialer/
│       │   └── MainActivity.kt    # SIP registration, calls, recording & quality metrics
│       └── res/
│           ├── drawable/          # Vector app icon & gradient UI assets
│           └── layout/
│               └── activity_main.xml # Main dialer & in-call UI layout
├── build.gradle
├── gradle.properties
└── settings.gradle
