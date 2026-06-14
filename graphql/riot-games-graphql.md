# Riot Games GraphQL Schema

This GraphQL schema provides a unified query interface over the Riot Games Developer API, covering League of Legends, VALORANT, Teamfight Tactics, Legends of Runeterra, and the cross-game Account API. The schema is derived from the REST endpoints documented at https://developer.riotgames.com/apis and the static data distributed via Data Dragon.

## Background

Riot Games exposes its game data through a collection of versioned REST APIs grouped by title. Developers register at the Riot Developer Portal to obtain an API key, which is scoped to one or more approved products. Rate limits are enforced at both the application and method levels. This GraphQL schema models the same underlying resources in a graph-oriented way so that a single query can traverse account identity, match history, participant stats, champion details, ranked standings, and live game data without multiple round trips.

## Schema Source

The schema was authored by reviewing:

- Riot Developer Portal API reference: https://developer.riotgames.com/apis
- Data Dragon static data documentation: https://developer.riotgames.com/docs/lol
- VALORANT API documentation: https://developer.riotgames.com/docs/valorant
- TFT API documentation: https://developer.riotgames.com/apis (TFT endpoints)
- GitHub organization: https://github.com/RiotGames

## Games and API Groups Covered

- **League of Legends** — Summoner, ChampionMastery, Match (v5), League/Ranked, LiveGame/Spectate, Clash, ChampionRotation
- **VALORANT** — ValorantMatch, ValorantRound, ValorantPlayer, ValorantTeam
- **Teamfight Tactics** — TFTMatch, TFTParticipant, TFTComposition, TFTAugment, TFTUnit
- **Cross-Game** — Account (PUUID resolution via Riot ID), Region, Platform, RateLimits, APIKey
- **Data Dragon** — Champion, ChampionDetail, ChampionStats, ChampionSkin, Skin, Chromas, SkinLine, ChampionRotation, Item, ItemDetail, ItemStat, ItemGold, Rune, RunePath, RuneSlot, SummonerSpell, ProfileIcon, ImageData, GameMap, GameMode, GameQueue

## Key Types

| Type | Description |
|------|-------------|
| Account | Cross-game Riot account with PUUID and Riot ID (gameName + tagLine) |
| PUUID | Opaque persistent unique identifier used across all Riot APIs |
| Summoner | League of Legends summoner profile linked to an Account |
| SummonerID | Encrypted summoner identifier scoped to a platform |
| SummonerName | In-game display name (deprecated in favor of Riot ID) |
| SummonerLevel | Summoner experience level |
| ProfileIcon | Profile icon image reference |
| Champion | Data Dragon champion entry with stats, skins, spells, and lore |
| ChampionDetail | Full champion data including passive and tips |
| ChampionStats | Base stat block for a champion |
| ChampionSkin | Skin variant for a champion |
| Skin | Extended skin metadata including skin line, rarity, and asset paths |
| Chromas | Chroma variants for a skin |
| SkinLine | Thematic collection grouping related skins |
| ChampionRotation | Weekly free champion rotation list |
| ChampionSpell | Champion ability definition from Data Dragon |
| ChampionPassive | Champion passive ability |
| Item | Data Dragon item with stats, gold cost, and build paths |
| ItemDetail | Item with resolved build-path item references |
| ItemStat | Flat and percent stat bonuses granted by an item |
| ItemGold | Item cost breakdown (base, total, sell) |
| Rune | Individual rune from a rune path |
| RunePath | Top-level rune path (Precision, Domination, etc.) |
| RuneSlot | Slot within a rune path containing selectable runes |
| SummonerSpell | Summoner spell definition from Data Dragon |
| Match | Full match record including metadata and detail |
| MatchDetail | Core match information with participants, teams, and game metadata |
| MatchTimeline | Frame-by-frame timeline of events within a match |
| MatchMetadata | Match identifier, data version, and participant PUUIDs |
| Team | Team-level result including bans and objectives |
| Participant | Full per-player stats within a match |
| ParticipantStats | Summary stat block for a participant |
| StatPerks | Rune page configuration used in a match |
| Perk | Individual rune selection with stat values |
| Ban | Champion ban in a draft phase |
| MatchEvent | Discrete event within a timeline frame |
| FrameData | Single timeline frame with events and participant frames |
| ChampionFrame | Per-champion snapshot within a timeline frame |
| KillEvent | Kill event detail within a timeline frame |
| ItemEvent | Item purchase or sale event within a timeline frame |
| Game | Lightweight game record with mode, map, and queue metadata |
| GameMap | Map identifier and display name |
| GameMode | Game mode identifier and description |
| GameQueue | Queue identifier, map, and description |
| LeagueEntry | A summoner's ranked entry in a specific queue |
| LeagueList | Full league roster for Challenger, Grandmaster, or Master |
| MiniSeries | Promotion series tracking for league advancement |
| Rank | Ranked tier subdivision (I through IV) |
| Tier | Ranked tier (Iron through Challenger) |
| Division | Alias for Rank used in some API contexts |
| LiveGame | Active game from the Spectator API |
| Spectate | Spectator access data including encryption key |
| SpectateParticipant | Participant record in a live game |
| Observer | Observer encryption key for a live game |
| Masteries | Collection of champion mastery records for a player |
| ChampionMastery | Individual champion mastery record |
| MasteryLevel | Mastery level (1–7) for a champion |
| ValorantMatch | Full VALORANT match record |
| ValorantRound | Individual round within a VALORANT match |
| ValorantPlayer | Player record within a VALORANT match |
| ValorantTeam | Team result within a VALORANT match |
| TFTMatch | Full Teamfight Tactics match record |
| TFTParticipant | Player result within a TFT match including placement and board |
| TFTComposition | Trait/synergy active for a TFT player |
| TFTAugment | Augment selected by a TFT player |
| TFTUnit | Individual unit on a TFT player's board |
| APIKey | Developer API key with rate limit configuration |
| RateLimits | Application and method rate limit caps |
| RateLimit | Single rate limit window (requests per seconds) |
| Region | Named routing region for Riot APIs |
| Platform | Platform endpoint within a region |
| ImageData | Data Dragon image sprite reference with URL |
| Position | Map coordinate for timeline events |

## Authentication

All Riot API requests require an `X-Riot-Token` header containing a valid API key obtained from https://developer.riotgames.com/. Personal API keys expire after 24 hours. Production keys are granted through the application process.

## Regional Routing

The Riot API uses two layers of routing:

- **Platform routing** (e.g., `na1`, `euw1`, `kr`) for summoner and live game endpoints
- **Regional routing** (e.g., `americas`, `europe`, `asia`) for match history and account endpoints

The `Region` and `Platform` types in this schema capture both layers.

## Rate Limiting

The Riot API enforces rate limits at the application level (shared across all methods) and the method level (per endpoint). Rate limits vary by key type (personal, development, production). The `RateLimits` type and `APIKey` type model these constraints.

## Files

| File | Description |
|------|-------------|
| `riot-games-schema.graphql` | Full GraphQL SDL schema with 75+ named types and a root Query type |
| `riot-games-graphql.md` | This documentation file |
