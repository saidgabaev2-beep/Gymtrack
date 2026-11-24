# Gymtrack

A responsive React fitness journal with workout logging, three starter routines, custom exercises, training volume charts, body measurements, scheduling and JSON export. All records stay in browser localStorage; there is no backend or account synchronization. Export important records regularly. Active workouts are in memory until finished.

## Development

Node.js 22+ recommended.

```sh
npm ci
npm run dev -- --port 5173
```

## Validation

```sh
npm run build
npx playwright install chromium
npm test
```

To use an installed Chromium instead of downloading a browser:

```sh
CHROMIUM_PATH=/usr/bin/chromium npm test
```

The browser test covers completing a workout, persistence after reload, measurements, scheduling and mobile overflow. Build output is in `dist/`, suitable for static hosting.

Weight defaults to kilograms and can be switched in settings. Completed workout volume and body weight are stored in kilograms and converted for display. Measurements use centimeters. This first version does not include cloud sync, backup import, photos, nutrition, rest timers or automated training advice.
