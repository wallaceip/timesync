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

## Getting Started

### Prerequisites

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
