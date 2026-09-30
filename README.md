# Winter Arc — Ink & Signal ❄️

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web-green.svg)]()
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)]()
[![Release](https://img.shields.io/badge/Release-v1.0.0-purple.svg)](release/winter-arc-v1.0.0.apk)

**Winter Arc** is an open-source, offline-first mobile application and habit mastery system designed for deep work, daily physical and mental discipline, financial tracking, and personal reflection.

Built with high-contrast neo-brutalist typography (*Space Grotesk*, *JetBrains Mono*, *DotGothic16*), dynamic haptics, and zero tracking or third-party telemetry.

---

## 📥 Download APK

You can download the pre-compiled Android APK directly from this repository:

- 📦 **[Download Winter Arc APK v1.0.0](winter-arc.apk)** *(Direct install on Android 7.0+)*
- 📁 Mirror in repository: [`release/winter-arc-v1.0.0.apk`](release/winter-arc-v1.0.0.apk)

To install on your Android device:
1. Transfer or download `winter-arc.apk` to your phone.
2. Tap the APK file to install (allow "Install from Unknown Sources" if prompted).
3. Open **Winter Arc** and begin your challenge.

---

## ✨ Features

- **🎯 Daily Habit Matrix**:
  - Track core disciplines (Morning affirmation, cold shower, nutrition, workout, outdoor run, sunrise wake).
  - Add custom habits with tailored accent colors.
  - Interactive SVG circular dial showing arc completion progress and streaks.
  - Hydration counter (8 glasses daily target) and daily top 3 priority task checklist.

- **💰 Money Ledger & Receipt**:
  - Log Income, Expenses, and Investments with instant category breakdowns.
  - Daily & weekly receipts with opening/closing balances and weekly savings rate.
  - Budget limits with visual overspend warnings.

- **📖 Reflective Journal**:
  - 4 guided templates: *Morning Intent*, *Evening Reflection*, *Money Mindset*, and *Free Write*.
  - Mood score tracking with daily habit and expenditure correlation.
  - Timeline history with fast lookup.

- **▦ Arc Master Sheet**:
  - Full matrix tracker for all 75 days of the challenge.
  - Weight tracking per day.
  - Customizable mark symbols (✓, ×, ●, ★, 🔥, ❄️, etc.).

- **🏆 Gamification & Medals**:
  - Rank system: Snowflake → Frostbite → Ice Walker → Blizzard → Glacier → Arctic Legend.
  - XP progression calculated from consistency, perfect days, journaling, and saving.
  - 15 unlockable milestone medals.

- **🔒 100% Private & Offline**:
  - All data stays locally on your device in secure storage.
  - Full JSON backup export and restore.
  - Formatted multi-tab Excel (`.xlsx`) report generation with embedded progress charts using bundled ExcelJS.

---

## 🛠️ Project Architecture

```
Winter Arc Open Source/
├── .github/
│   └── workflows/
│       └── build-apk.yml        # CI/CD: Automated APK build & GitHub Releases
├── android/                     # Native Android project (Capacitor + Gradle)
│   ├── app/
│   │   ├── src/main/            # AndroidManifest, assets, Java sources, icons
│   │   └── build.gradle         # Application gradle configuration
│   └── gradlew.bat              # Gradle wrapper script
├── www/                         # Clean, bundled web application
│   ├── index.html               # Main application interface & logic
│   └── js/
│       └── exceljs.min.js       # Bundled offline Excel generation library
├── release/
│   └── winter-arc-v1.0.0.apk    # Compiled release-ready APK
├── winter-arc.apk               # Root ready-to-install APK file
├── capacitor.config.json        # Capacitor native bridge settings
├── package.json                 # Node dependencies and build scripts
├── CONTRIBUTING.md              # Open source contribution guide
├── LICENSE                      # MIT Open Source License
└── README.md                    # Documentation
```

---

## 🚀 Building from Source

### Prerequisites
- [Node.js](https://nodejs.org/) (v18+)
- [Java JDK](https://adoptium.net/) (v17 or v21)
- [Android SDK](https://developer.android.com/studio) (API 34 or 35)

### Build Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/winter-arc.git
   cd winter-arc
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Sync web assets with the native Android project**:
   ```bash
   npm run sync
   ```

4. **Compile the APK**:
   ```bash
   npm run build:apk
   ```
   The generated APK will be at:
   `android/app/build/outputs/apk/debug/app-debug.apk`

---

## 🌐 Publishing to GitHub

To maintain and publish this project on GitHub:

1. **Create a new repository** on GitHub (e.g. `winter-arc`).
2. **Push your code**:
   ```bash
   git init
   git add .
   git commit -m "feat: initial open-source release v1.0.0"
   git remote add origin https://github.com/your-username/winter-arc.git
   git branch -M main
   git push -u origin main
   ```
3. **Automated Releases**:
   Whenever you push a tag (e.g. `v1.0.0`), the included GitHub Action (`.github/workflows/build-apk.yml`) will automatically build the APK and attach it directly to a new GitHub Release!
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, distribute, and contribute.
