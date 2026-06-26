# 💷 Currency Calculator

A lightweight currency converter built with vanilla JavaScript. It shows live
exchange rates, converts between currencies in real time, and draws a 7‑day
trend chart for each side of the conversion.

**Live demo:** https://elkhan-isayev.github.io/currency-calculator-js/

## Features

- 🔄 Real‑time conversion between two currencies
- 💱 30+ currencies, picked from a modal list
- 📈 Weekly exchange‑rate trend charts (powered by Chart.js)
- ↔️ One‑click swap ("castling") of the two currencies
- 🌐 No API key required — uses the free [Frankfurter](https://frankfurter.dev) API
  (the successor of the now‑defunct `ratesapi.io`)

## Tech stack

- Vanilla JavaScript (ES modules), bundled with **webpack 5** + **Babel**
- [Chart.js 4](https://www.chartjs.org/) for the trend charts
- [Day.js](https://day.js.org/) for date handling
- [Frankfurter API](https://frankfurter.dev) for exchange‑rate data

## Getting started

Requires [Node.js](https://nodejs.org/) 18+.

```bash
# install dependencies
npm install

# build the development bundle into dist/
npm run build

# build the minified production bundle into dist/
npm run build:prod
```

Then open `index.html` in a browser (or serve the folder with any static file
server, e.g. `npx serve`).

## Project structure

```
.
├── index.html         # markup
├── index.js           # application logic (entry point)
├── css/               # styles
├── assets/            # images / icons
├── dist/              # webpack build output (generated, git‑ignored)
└── webpack.config.js
```

## Deployment

The site is deployed automatically to **GitHub Pages** on every push to
`master` via the workflow in [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml),
which builds the production bundle and publishes the static files.

To enable it on a fork: open **Settings → Pages → Build and deployment** and set
the source to **GitHub Actions**.

## License

ISC © Elkhan Isayev
