# NCAA Volleyball Scoreboard

A single-page web application that displays NCAA Division I Men's and Women's indoor volleyball schedules and scores for the current week (Monday–Sunday).

## Features

- **Full week view** — shows all games for the current Mon–Sun week, not just today
- **Date groupings** — games are grouped by day with a date divider; today is highlighted
- **Live scores** — in-progress games show a live indicator with current set detail
- **Final scores** — completed games display the final score with the winner highlighted
- **Upcoming games** — scheduled games show their tip-off time in Eastern time
- **Broadcast info** — each game shows the TV channel or streaming service it airs on
- **Team details** — team logos, rankings (if top 25), and venue information
- **Auto-refresh** — scores update automatically every 60 seconds

## Data Source

Scores and schedules are pulled from ESPN's public scoreboard API. Only the two NCAA Division I indoor volleyball leagues (men's and women's) are available through this API.

## Hosted (HTTPS)

The scoreboard is publicly available over HTTPS via GitHub Pages:

**https://allensell.github.io/ncaa-volleyball-scoreboard/**

## Running locally

Serve it with a local HTTPS-ready server to get proper security headers:

```bash
npm start
```

This runs `npx serve` on port 8080 with the headers defined in `serve.json`.  
Open **http://localhost:8080** in your browser.

No `npm install` needed — `npx` fetches `serve` automatically on first run.

## Security headers (serve.json)

When served through `npm start`, the following headers are applied:

| Header | Value |
|---|---|
| `Content-Security-Policy` | Restricts connections to ESPN API only; blocks inline frames |
| `X-Frame-Options` | `DENY` — prevents clickjacking |
| `X-Content-Type-Options` | `nosniff` |
| `X-XSS-Protection` | `1; mode=block` |
| `Referrer-Policy` | `strict-origin-when-cross-origin` |
| `Permissions-Policy` | Disables geolocation, microphone, camera |
