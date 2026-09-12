# ⏱ TimeSync

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
- **Multiple profiles** — separate players each get their own history, settings, and stats
- **Configurable time ranges** — adjust min/max target times for both stopwatch and beep modes per profile
- **Haptic feedback & audio cues** — tactile responses on interactions and audio playback for beep mode

## Tech Stack

- **Framework:** [Expo](https://expo.dev) (SDK 57) with [Expo Router](https://docs.expo.dev/router/introduction/)
- **Language:** TypeScript
- **UI:** React Native with `react-native-reanimated` and `react-native-gesture-handler`
- **Storage:** `@react-native-async-storage/async-storage`
- **Platform support:** iOS, Android, Web

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS version recommended)
- [Expo Go](https://expo.dev/go) on your physical device, or a configured iOS Simulator / Android Emulator

### Install & Run

```bash
git clone https://github.com/wallaceip/timesync.git
cd timesync
npm install
npx expo start
```

- **Physical device:** Scan the QR code with Expo Go (Android) or the Camera app (iOS)
- **Android Emulator:** Press `a` in the terminal
- **iOS Simulator:** Press `i` in the terminal (macOS required)
- **Web browser:** Press `w` in the terminal

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

## Available Scripts

- `npx expo start` — Start the Expo development server
- `npm run android` — Launch on a connected Android device or emulator
- `npm run ios` — Launch in the iOS simulator
- `npm run web` — Run in a web browser

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -m 'Add NewFeature'`)
4. Push to your branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

## License

MIT
