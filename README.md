# ⏱ TimeSync

<<<<<<< HEAD
A mobile app that trains your internal clock through timing-based mini-games. Built with React Native and Expo.

## Game Modes

### Blind Stopwatch
See a target time, memorize it, then start a hidden timer. Stop it when you think you've hit the target — the display stays dark while the timer runs.

### Beep Interval
Listen for two audio beeps and estimate the time between them using a numpad. Tests auditory time perception instead of visual.

### Stopwatch Duel
Split-screen 1v1 on a single device. Both players see the same target time, start and stop their own timers independently, and the closest one wins. Uses gesture-based multitouch so both halves work simultaneously.

## Features

- **Centisecond precision** — all game modes track accuracy down to 0.01s
- **Per-game scoring** — rated on how close you land (within 0.1s, 0.5s, 1s, etc.)
- **History & analytics** — tracks games played, average error, best score, and ≤1s accuracy percentage with a bar chart of recent performance
- **Multiple profiles** — separate players each get their own history, settings, and stats (stored via AsyncStorage)
- **Configurable time ranges** — adjust min/max target times for both stopwatch and beep modes per profile
- **Haptic feedback** — uses `expo-haptics` for tactile responses on interactions
- **Audio cues** — `expo-audio` for beep interval playback

## Tech Stack

- **Framework:** [Expo](https://expo.dev) (SDK 57) with [Expo Router](https://docs.expo.dev/router/introduction/)
- **Language:** TypeScript
- **UI:** React Native with `react-native-reanimated` and `react-native-gesture-handler`
- **Storage:** `@react-native-async-storage/async-storage`
- **Platform support:** iOS, Android, Web
=======
A mobile timing and synchronization application built with React Native and Expo. TimeSync tests precision and reaction time through clock synchronization mechanics and interactive timing challenges.

## Features

- **Precision Timing Mechanics:** Accurate millisecond tracking for reflex and synchronization challenges.
- **Cross-Platform Support:** Native performance across Android, iOS, and Web via Expo.
- **Clean Mobile UI:** Intuitive, touch-friendly interface designed for rapid interaction.
- **Dynamic Feedback:** Real-time scoring, latency/offset calculation, and round results.

## Tech Stack

- **Framework:** React Native
- **Platform:** Expo
- **Language:** JavaScript / TypeScript
- **Styling:** React Native StyleSheet

## Prerequisites

Before running the application, ensure you have the following installed:

- **Node.js** (LTS version recommended)
- **npm** or **yarn**
- **Expo Go** app on your physical iOS or Android device (available on Google Play Store and Apple App Store), or a configured iOS Simulator / Android Emulator.
>>>>>>> 38b03dc094e02abd76e67aa7cfae920f67d4fdb7

## Getting Started

### 1. Clone the Repository

<<<<<<< HEAD
- [Node.js](https://nodejs.org/) (v18+)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)

### Install & Run

```bash
git clone https://github.com/wallaceip/timesync.git
cd timesync
npm install
npx expo start
```

Scan the QR code with [Expo Go](https://expo.dev/go) or press `a` / `i` to open on an Android emulator or iOS simulator.

## Project Structure

```
app/
├── _layout.tsx          # Root stack navigator
├── index.tsx            # Home screen with game mode cards
├── stopwatch.tsx        # Blind Stopwatch mode
├── beep.tsx             # Beep Interval mode
├── stopwatch-duel.tsx   # 1v1 split-screen duel
├── history.tsx          # Game history & analytics
├── profiles.tsx         # Profile management
└── settings.tsx         # Time range config & data management
components/
├── BarChart.tsx          # Error-per-game chart
├── GameCard.tsx          # Home screen mode selector
├── GlowButton.tsx        # Themed action button
├── NumPad.tsx            # In-game numpad input
├── ScoreResult.tsx       # Post-game score breakdown
└── TimerDisplay.tsx      # Formatted time display
utils/
├── sounds.ts            # Audio playback
├── storage.ts           # AsyncStorage CRUD, profiles, settings
└── timeHelpers.ts       # Time formatting, scoring, RNG
```

## License

MIT
=======
```bash
git clone [https://github.com/wallaceip/timesync.git](https://github.com/wallaceip/timesync.git)
cd timesync

```

### 2. Install Dependencies

```bash
npm install

```

### 3. Start the Development Server

```bash
npx expo start

```

### 4. Run the Application

Once the Metro bundler starts in your terminal:

* **On a Physical Device:** Scan the displayed QR code using the **Expo Go** app (Android) or the native **Camera** app (iOS).
* **On Android Emulator:** Press `a` in the terminal.
* **On iOS Simulator:** Press `i` in the terminal (macOS required).
* **In Web Browser:** Press `w` in the terminal.

## Project Structure

```text
timesync/
├── assets/          # App icons, splash screens, and static images
├── components/      # Reusable UI elements (timers, buttons, display cards)
├── screens/         # Main application views and game screens
├── App.js           # Root application entry and state setup
├── app.json         # Expo configuration and metadata
├── package.json     # Project dependencies and run scripts
└── README.md        # Documentation

```

## Available Scripts

* `npx expo start` - Start the Expo development server.
* `npx expo start --clear` - Clear Metro bundler cache before starting.
* `npm run android` - Start the project directly on a connected Android device or emulator.
* `npm run ios` - Start the project directly in the iOS simulator.
* `npm run web` - Run the app in a web browser.

## Contributing

Contributions, bug reports, and feature suggestions are welcome:

1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -m 'Add NewFeature'`).
4. Push to your branch (`git push origin feature/NewFeature`).
5. Open a Pull Request.
>>>>>>> 38b03dc094e02abd76e67aa7cfae920f67d4fdb7
