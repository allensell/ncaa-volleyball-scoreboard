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

## Usage

Open `ncaa_volleyball_scores.html` directly in any web browser — no server or build step required. An internet connection is needed to fetch live data.
