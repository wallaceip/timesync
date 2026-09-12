# ⏱ TimeSync

A cross-platform mobile application that helps users develop time estimation skills through interactive mini-games. Each mode presents a timing challenge — estimate durations, react to audio cues, or compete head-to-head — and provides detailed scoring and analytics to track improvement over time.

Built with React Native and Expo. Supports iOS, Android, and web.

## Game Modes

**Blind Stopwatch** — A target duration is displayed briefly, then the screen goes dark. The user starts a hidden timer and must stop it when they believe the target time has elapsed.

**Beep Interval** — Two audio beeps play separated by a randomized interval. The user estimates the elapsed time between them and submits their answer via an on-screen numpad.

**Stopwatch Duel** — A split-screen 1v1 mode for two players on a single device. Both players see the same target duration and independently start and stop their own timers. The player closest to the target wins. Implemented with gesture-based multitouch to support simultaneous input on both halves of the screen.

## Features

- **Centisecond precision** — all modes track accuracy to 0.01s
- **Tiered scoring** — performance is graded based on proximity to the target (within 0.1s, 0.5s, 1s, etc.)
- **History & analytics** — tracks games played, average error, best score, and ≤1s accuracy rate with a per-game bar chart
- **Multiple profiles** — each player has independent history, statistics, and settings
- **Configurable difficulty** — adjustable min/max target time ranges per profile for both stopwatch and beep modes
- **Haptic feedback & audio cues** — tactile responses on interactions; audio playback for beep mode

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended)
- [Expo Go](https://expo.dev/go) on a physical device, or a configured iOS Simulator / Android Emulator

### Installation

```bash
git clone https://github.com/wallaceip/timesync.git
cd timesync
npm install
npx expo start
```

Once the dev server is running:

- **Physical device** — scan the QR code with Expo Go (Android) or the Camera app (iOS)
- **Android Emulator** — press `a` in the terminal
- **iOS Simulator** — press `i` (macOS only)
- **Web** — press `w`

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | [Expo](https://expo.dev) SDK 57 with [Expo Router](https://docs.expo.dev/router/introduction/) |
| Language | TypeScript |
| UI | React Native, `react-native-reanimated`, `react-native-gesture-handler` |
| Storage | `@react-native-async-storage/async-storage` |

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
├── BarChart.tsx          # Per-game error chart
├── GameCard.tsx          # Home screen mode selector
├── GlowButton.tsx        # Themed action button
├── NumPad.tsx            # On-screen numpad input
├── ScoreResult.tsx       # Post-game score breakdown
└── TimerDisplay.tsx      # Formatted time display
utils/
├── sounds.ts            # Audio playback
├── storage.ts           # AsyncStorage CRUD, profiles, settings
└── timeHelpers.ts       # Time formatting, scoring, RNG
```

## Scripts

| Command | Description |
|---------|-------------|
| `npx expo start` | Start the Expo development server |
| `npm run android` | Launch on a connected Android device or emulator |
| `npm run ios` | Launch in the iOS Simulator |
| `npm run web` | Run in a web browser |

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

MIT
