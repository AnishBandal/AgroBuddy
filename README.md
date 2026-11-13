<div align="center">

  <img src="app/src/main/res/drawable/agrobuddy_logo.jpg" alt="AgroBuddy logo" width="120" />

  # AgroBuddy

  ### 🌱 One community for the people who grow, trade, and enjoy food

  An agriculture-focused Android application connecting **farmers**, **traders**, and **consumers** through products, knowledge, requests, and conversations.

  <p>
    <img src="https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white" alt="Android" />
    <img src="https://img.shields.io/badge/language-Java-orange?logo=java&logoColor=white" alt="Java" />
    <img src="https://img.shields.io/badge/compile%20SDK-34-4285F4?logo=android&logoColor=white" alt="Compile SDK 34" />
    <img src="https://img.shields.io/badge/backend-Firebase-FFCA28?logo=firebase&logoColor=black" alt="Firebase" />
    <img src="https://img.shields.io/badge/license-not%20specified-lightgrey" alt="License not specified" />
  </p>

  <p>
    <a href="#-features">Features</a> •
    <a href="#-getting-started">Getting started</a> •
    <a href="#-development">Development</a> •
    <a href="#-security">Security</a>
  </p>

</div>

> [!NOTE]
> AgroBuddy is currently an Android/Gradle project. The Firebase configuration file is intentionally kept local and is not committed to Git.

## ✨ Features

| 👨‍🌾 For farmers | 🏪 For traders | 🛒 For consumers |
|---|---|---|
| Publish products and seeds | Discover available products | Browse agricultural listings |
| Manage incoming requests | Request seeds and products | Submit product requests |
| Share farming knowledge | Chat with other users | Read blogs and community posts |
| Access crop disease assistance | Maintain a user profile | Connect with the agriculture community |

### Community and smart tools

<table>
  <tr>
    <td>🔐 <strong>Authentication</strong><br />Firebase sign-in with OTP verification.</td>
    <td>💬 <strong>Messaging</strong><br />Direct chat between community members.</td>
    <td>📰 <strong>Content</strong><br />Posts, comments, blogs, and news.</td>
  </tr>
  <tr>
    <td>📍 <strong>Location</strong><br />Location-aware agriculture workflows.</td>
    <td>📷 <strong>Media</strong><br />Camera and image upload support.</td>
    <td>🩺 <strong>Plant health</strong><br />TensorFlow Lite disease assistance.</td>
  </tr>
</table>

## 🧭 App flow

```mermaid
flowchart LR
    A[🌱 Splash screen] --> B[🔐 Login / Register]
    B --> C{Choose role}
    C --> D[👨‍🌾 Farmer home]
    C --> E[🏪 Trader home]
    C --> F[🛒 Consumer home]
    D --> G[Products · Seeds · Requests]
    E --> G
    F --> G
    G --> H[💬 Chat · Posts · Blogs]
```

## 🧰 Technology stack

| Area | Tools |
|---|---|
| Platform | Android |
| Language | Java |
| UI | XML layouts, AndroidX, Material Components, RecyclerView |
| Backend | Firebase Authentication, Cloud Firestore, Firebase Storage, Firebase Analytics |
| Machine learning | TensorFlow Lite |
| Python integration | Chaquopy with Python 3.10 |
| Build | Gradle and Android Gradle Plugin |

## 📁 Project structure

```text
.
├── app/
│   ├── src/main/java/com/example/Farmer/   # Activities, fragments, models, adapters
│   ├── src/main/res/                       # Layouts, drawables, themes, and assets
│   ├── src/main/python/                    # Python utilities
│   ├── build.gradle
│   └── google-services.json                # Local Firebase configuration
├── gradle/
├── build.gradle
├── gradle.properties
├── settings.gradle
├── gradlew
└── gradlew.bat
```

## 🚀 Getting started

### Prerequisites

| Requirement | Version |
|---|---|
| Android Studio | Hedgehog or newer |
| Android SDK | 34 |
| JDK | 8 or compatible Android Studio JDK |
| Python | 3.10 |
| Firebase | Android project with Auth, Firestore, and Storage enabled |

### Installation

1. Open the project in Android Studio.
2. Create or select a Firebase project.
3. Enable **Firebase Authentication**, **Cloud Firestore**, and **Firebase Storage**.
4. Download the Firebase Android configuration file.
5. Place it at:

   ```text
   app/google-services.json
   ```

6. Sync Gradle, select an emulator or device, and run the `app` configuration.

<details>
<summary>🛠️ Build from the command line</summary>

**macOS/Linux**

```bash
./gradlew assembleDebug
```

**Windows**

```bat
gradlew.bat assembleDebug
```

The debug APK is written to `app/build/outputs/apk/debug/`.

</details>

## 🧪 Development

Run unit tests:

```bash
./gradlew test
```

Run connected Android tests with an emulator or physical device:

```bash
./gradlew connectedAndroidTest
```

<details>
<summary>🔒 Required Android permissions</summary>

Depending on the workflow, AgroBuddy may request:

- Internet access
- Camera access
- Fine and coarse location
- Image/media access

Grant permissions only when the related feature needs them.

</details>

## 🔐 Security

- Never commit `google-services.json`, signing keys, passwords, API keys, or local configuration.
- Configure and review Firebase security rules before using production data.
- Use a separate Firebase project for development and testing.

## 📄 License

No license has been specified yet. Add a license before distributing AgroBuddy or accepting external contributions.

<div align="center">

  <sub>Built with 🌾 for a more connected agriculture community.</sub>

</div>
