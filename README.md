# Riot Games

Riot Games provides a comprehensive developer platform for accessing game data across League of Legends, VALORANT, Teamfight Tactics, Legends of Runeterra, and other titles. The Riot Developer Portal offers REST APIs for match history, ranked standings, champion mastery, live spectator data, tournament management, and player account data.

## APIs

### League of Legends API
API for accessing League of Legends game data including champion mastery, clash tournaments, ranked league standings, match history, live spectator data, summoner profiles, and tournament management.

- **Base URL:** `https://na1.api.riotgames.com` (regional variants available)
- **Documentation:** https://developer.riotgames.com/apis
- **Authentication:** API Key (`X-Riot-Token` header)

### VALORANT API
API for accessing VALORANT game data including match history, ranked standings, content catalog, and status information.

- **Documentation:** https://developer.riotgames.com/docs/valorant

### Teamfight Tactics API
API for accessing Teamfight Tactics game data including match history, ranked standings, summoner profiles, and live spectator data.

- **Documentation:** https://developer.riotgames.com/apis

### Legends of Runeterra API
API for accessing Legends of Runeterra game data including player decks, inventory, match history, and ranked standings.

- **Documentation:** https://developer.riotgames.com/docs/lor

### Riot Account API
Cross-game account API for resolving Riot IDs to PUUIDs used across all Riot Games APIs.

- **Base URL:** `https://americas.api.riotgames.com`
- **Documentation:** https://developer.riotgames.com/apis

### Data Dragon
Static data and asset delivery service providing localized game data for champions, items, summoner spells, and maps. Updated with each patch.

- **Base URL:** `https://ddragon.leagueoflegends.com/cdn`
- **Documentation:** https://developer.riotgames.com/docs/lol

## OpenAPI Specifications

| API | Specification |
|-----|---------------|
| League of Legends API | [riot-games-league-of-legends-openapi.yml](openapi/riot-games-league-of-legends-openapi.yml) |

## Capabilities

Naftiko capability definitions for AI-assisted gaming analytics workflows:

| Capability | Description |
|------------|-------------|
| [Game Data Analytics](capabilities/game-data-analytics.yaml) | Player lookup, match history, champion mastery, ranked standings, live game |

### Shared Definitions

| Definition | API |
|------------|-----|
| [league-of-legends.yaml](capabilities/shared/league-of-legends.yaml) | League of Legends API |

## Rules

Spectral ruleset for validating Riot Games API conventions:

- [riot-games-rules.yml](rules/riot-games-rules.yml)

## JSON Schemas

| Schema | Description |
|--------|-------------|
| [riot-games-summoner-schema.json](json-schema/riot-games-summoner-schema.json) | Summoner profile record |
| [riot-games-match-schema.json](json-schema/riot-games-match-schema.json) | Match record from Match v5 API |

## JSON Structures

| Structure | Description |
|-----------|-------------|
| [riot-games-match-structure.json](json-structure/riot-games-match-structure.json) | Field documentation for match records |

## JSON-LD

| Context | Description |
|---------|-------------|
| [riot-games-context.jsonld](json-ld/riot-games-context.jsonld) | Linked data context for Riot Games player, match, and champion entities |

## Examples

| Example | Description |
|---------|-------------|
| [riot-games-get-summoner-example.json](examples/riot-games-get-summoner-example.json) | Get summoner by PUUID |
| [riot-games-get-match-example.json](examples/riot-games-get-match-example.json) | Get match details |

## Vocabulary

- [riot-games-vocabulary.yml](vocabulary/riot-games-vocabulary.yml) — Domain vocabulary for Riot Games APIs covering player identity, gameplay, ranking, and infrastructure

## Links

- **Developer Portal:** https://developer.riotgames.com/
- **API Reference:** https://developer.riotgames.com/apis
- **Rate Limiting Guide:** https://developer.riotgames.com/docs/portal
- **GitHub:** https://github.com/RiotGames
- **Terms of Service:** https://developer.riotgames.com/policies/general
