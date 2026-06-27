# QuitSmoking

A SwiftUI iOS app to help you manage and reduce smoking by enforcing minimum intervals between cigarettes.

## How It Works

The app tracks your smoking habits and enforces a configurable minimum interval between cigarettes:

1. **Tap "Can I smoke now?"** — The app checks if enough time has passed since your last cigarette
2. **If too soon** — You're told to wait, and the next available time is extended slightly as a "punishment"
3. **If it's time** — You can smoke, and the app records it
4. **Extra cigarettes** — You get a limited number of "extra" cigarettes per day (default: 4) for emergencies

## Features

- **Interval enforcement** — Default 15-minute cooldown between cigarettes
- **Daily tracking** — Counts how many you've smoked today
- **Total tracking** — Cumulative lifetime count
- **Spending tracker** — Calculates money spent on cigarettes
- **Extra cigarettes** — A limited daily reserve for when you really need one
- **Persistent data** — Uses UserDefaults to save your history

## Data

The app stores data in `UserDefaults`:

| Key | Type | Description |
|---|---|---|
| `extra` | Int | Extra cigarettes remaining today |
| `smokedToday` | Int | Cigarettes smoked today |
| `smokedTotal` | Int | Total cigarettes smoked |
| `spent` | Int | Money spent on cigarettes |
| `next` | Date | When you can smoke again |
| `interval` | TimeInterval | Cooldown between cigarettes (default: 900s / 15min) |
| `punishment` | Double | Extra time multiplier when smoking too early (default: 0.2 = 20%) |

## Requirements

- iOS 13.0+
- Xcode 11+

## Author

Fernando Oliveira

## License

MIT
