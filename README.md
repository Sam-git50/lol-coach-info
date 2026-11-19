# LoL Pro Configurator

A personal, non-commercial tool for League of Legends that runs locally on my own computer. This repository is only a public description of the project (no code, no personal data).

## What it does
- **Champion-select assistant**: ranks pick suggestions by combining current patch statistics with my own mastery of each champion.
- **Rune and build planning**: build and rune labs with computed stats and strengths/weaknesses analysis.
- **Offline draft simulator**: practice drafts for both sides or against an AI opponent.
- **Personal stats tracking**: win rate, KDA, CS/min and trends from my own games.

## Use of the Riot API
- League-v4 (ranked entries), Match-v5 (match IDs and details) and, as a fallback only, Summoner-v4.
- The tool samples a small number of recent ranked solo/duo matches from a chosen tier and aggregates them into per-patch champion statistics: win rate, pick rate, ban rate and lane matchup win rates.
- Only these aggregated numbers and processed match IDs (to avoid duplicates) are stored, locally. Player identifiers are used transiently to fetch matches and are not stored or displayed.
- Static data (champions, items, runes, images) comes from Data Dragon.

## Compliance
- Single user, runs locally, not publicly hosted, no accounts, no ads, no monetization.
- The API key is kept in a local environment file and is never shared or exposed.
- Requests respect the documented rate limits (20 requests/second, 100 requests/2 minutes) and the `Retry-After` header on HTTP 429. Collection is small, user-triggered or weekly.
- No scraping of third-party sites.

*LoL Pro Configurator isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or registered trademarks of Riot Games, Inc.*
