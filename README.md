# Riot Games (riot-games)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Riot Games provides a comprehensive developer platform for accessing game data across League of Legends, VALORANT, Teamfight Tactics, Legends of Runeterra, and other titles. The Riot Developer Portal offers REST APIs for match history, ranked standings, champion mastery, live spectator data, tournament management, and player account data.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Esports
- Gaming
- League of Legends
- Legends of Runeterra
- Teamfight Tactics
- VALORANT

## Timestamps

- **Created:** 2025-02-08
- **Modified:** 2026-05-19

## APIs

### League of Legends API

API for accessing League of Legends game data including champion mastery, clash tournaments, ranked league standings, match history, live spectator data, summoner profiles, and tournament management. All APIs are currently version 4 or 5.

- **Human URL:** [https://developer.riotgames.com/apis](https://developer.riotgames.com/apis)
- **Base URL:** `https://na1.api.riotgames.com`

#### Tags

- Champion Mastery
- Clash
- League of Legends
- Match History
- Ranked
- Summoner
- Tournaments

#### Properties

- [Documentation](https://developer.riotgames.com/apis)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/openapi/riot-games-league-of-legends-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### VALORANT API

API for accessing VALORANT game data including match history, ranked standings, content catalog, and status information. Covers both PC and console platforms.

- **Human URL:** [https://developer.riotgames.com/apis](https://developer.riotgames.com/apis)
- **Base URL:** `https://na.api.riotgames.com`

#### Tags

- Console
- Match History
- Ranked
- VALORANT

#### Properties

- [Documentation](https://developer.riotgames.com/docs/valorant)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Teamfight Tactics API

API for accessing Teamfight Tactics game data including match history, ranked standings, summoner profiles, and live spectator data for the auto battler game mode.

- **Human URL:** [https://developer.riotgames.com/apis](https://developer.riotgames.com/apis)
- **Base URL:** `https://na1.api.riotgames.com`

#### Tags

- Match History
- Ranked
- Summoner
- Teamfight Tactics

#### Properties

- [Documentation](https://developer.riotgames.com/apis)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Legends of Runeterra API

API for accessing Legends of Runeterra game data including player decks, inventory, match history, and ranked standings. Requires Riot Sign-On (RSO) authentication for player-specific data.

- **Human URL:** [https://developer.riotgames.com/apis](https://developer.riotgames.com/apis)
- **Base URL:** `https://americas.api.riotgames.com`

#### Tags

- Decks
- Legends of Runeterra
- Match History
- Ranked

#### Properties

- [Documentation](https://developer.riotgames.com/docs/lor)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Riot Account API

Cross-game account API for resolving Riot IDs (gameName + tagLine) to PUUIDs used across all Riot Games APIs. Supports account linking through Riot Sign-On (RSO) OAuth 2.0 authentication.

- **Human URL:** [https://developer.riotgames.com/apis](https://developer.riotgames.com/apis)
- **Base URL:** `https://americas.api.riotgames.com`

#### Tags

- Account
- Authentication
- Identity
- PUUID

#### Properties

- [Documentation](https://developer.riotgames.com/apis)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Riot Data Dragon

Static data and asset delivery service for Riot Games. Provides localized game data for champions, items, summoner spells, runes, profile icons, and maps in JSON format. Available in 28+ languages. Updated with each game patch.

- **Human URL:** [https://developer.riotgames.com/docs/lol](https://developer.riotgames.com/docs/lol)
- **Base URL:** `https://ddragon.leagueoflegends.com/cdn`

#### Tags

- Champions
- Data Dragon
- Items
- Static Data

#### Properties

- [Documentation](https://developer.riotgames.com/docs/lol)
- [Postman Collection](collections/riot-games-league-of-legends.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/riot-games-league-of-legends.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/riot-games)
- [Developer](https://developer.riotgames.com/)
- [Documentation](https://developer.riotgames.com/apis)
- [Authentication](https://developer.riotgames.com/docs/portal)
- [Rate Limiting](https://developer.riotgames.com/docs/portal)
- [Github Org](https://github.com/RiotGames)
- [Sign Up](https://developer.riotgames.com/)
- [Terms of Service](https://developer.riotgames.com/policies/general)
- [Privacy Policy](https://www.riotgames.com/en/privacy-notice)
- [Website](https://www.riotgames.com)
- [Spectral Rules](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/rules/riot-games-rules.yml)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/json-schema/riot-games-summoner-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/json-schema/riot-games-match-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N L D Context](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/json-ld/riot-games-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/vocabulary/riot-games-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
