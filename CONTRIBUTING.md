# Contributing to Winter Arc

Thank you for your interest in contributing to Winter Arc! This is an open-source, offline-first personal tracker designed to help people build discipline, stay grounded, and track their growth.

## How to Contribute

1. **Fork the Repository**: Click "Fork" on GitHub to create your own copy.
2. **Clone your Fork**:
   ```bash
   git clone https://github.com/your-username/winter-arc.git
   cd winter-arc
   ```
3. **Install Dependencies**:
   ```bash
   npm install
   ```
4. **Make Your Changes**:
   - The core web interface lives in `www/index.html`.
   - Update styles, views, or native Capacitor configuration as needed.
5. **Sync with Android**:
   ```bash
   npm run sync
   ```
6. **Build & Test the APK**:
   ```bash
   npm run build:apk
   ```
   Or open Android Studio:
   ```bash
   npm run open:android
   ```
7. **Submit a Pull Request**:
   - Create a feature branch: `git checkout -b feature/my-new-feature`
   - Commit your changes with clear messages.
   - Push to your fork and submit a PR!

## Guidelines
- Keep the app **100% offline-first**: all core features must work without an internet connection.
- Preserve the minimalist, ink & signal aesthetic and high performance.
- Respect user privacy: never collect or transmit telemetry or user tracking data.
