# ProFormance

Personal esports performance analytics platform for tracking professional League of Legends player form and statistical trends.

## What it does

ProFormance monitors a watchlist of professional LoL players, aggregates their ranked match history via the Riot API, and computes rolling performance baselines. When a player's recent form deviates significantly from their established baseline, the tool flags it for review.

## Features

- **Player watchlist** — Track LCK, LPL, LEC, and LCS professionals by Riot ID
- **Match history ingestion** — Hourly polling via Riot Match v5 API
- **Rolling baselines** — Configurable windows (default: 30 games) across KDA, CS/min, damage share, vision score/min, gold/min
- **Anomaly detection** — Z-score based flagging when recent form (last 3 games) deviates ≥2σ from baseline
- **Activity monitoring** — Detects changes in play frequency before major tournaments

## APIs Used

- `riot/account/v1` — PUUID resolution by Riot ID
- `lol/match/v5` — Match history and detailed game data

All data is fetched on a scheduled basis and stored locally. No data is redistributed or displayed publicly.

## Stack

- Node.js
- Riot Games API (Match v5, Account v1)
- Local JSON data store

## Status

Personal research project. Not affiliated with Riot Games.
