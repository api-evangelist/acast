# Acast (acast)

Acast is a podcast hosting, distribution, and advertising marketplace that helps creators publish shows, distribute to every major listening platform, and monetize through dynamic ad insertion and sponsorships. Acast exposes a documented public **Publishing API** for programmatically managing shows and episodes - listing shows and episodes, fetching details, and creating, updating, and deleting episodes - plus placing ad markers and receiving webhook notifications for events like new episode publications.

**Access model (honest note):** The Publishing API is documented openly at [developers.acast.com](https://developers.acast.com/), but it is **access-gated**. You authenticate with an `X-API-Key` header, and that key is issued by Acast's customer success team. API access is only available to accounts on the **Ace** plan or in the **Acast Creator Network**; the free Starter and mid-tier Influencer plans do not include API access. API keys are scoped to a user and grant access only to the shows assigned to that user.

The specific endpoint paths in this catalog's OpenAPI are **modeled** from Acast's documented resource operations (list shows, get show, list/get/create/update/delete episodes, PATCH ad markers). The public documentation confirms the resources, HTTP methods, base host (`api.acast.com`), authentication header, and rate limit, but the full path/schema reference is served behind an interactive viewer that requires credentials. Modeled endpoints are flagged with `x-endpointsModeled: true` in the OpenAPI document.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/acast/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/acast/refs/heads/main/apis.yml)

## Tags

- Podcasting
- Podcast Hosting
- Publishing
- Advertising
- Monetization
- Media
- Audio

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Acast Shows API

List all shows in a network and fetch details for a specific show. Read-only access to show metadata (title, description, artwork, RSS feed, and episode listings) scoped to the shows assigned to the API key's user.

- **Human URL:** [https://developers.acast.com/](https://developers.acast.com/)
- **Base URL:** `https://api.acast.com`

#### Tags

- Shows
- Podcasts
- Publishing

#### Properties

- [Documentation](https://developers.acast.com/)
- [API Reference](https://learn.acast.com/en/articles/5790019-acast-publishing-api)
- [OpenAPI](openapi/acast-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Acast Episodes API

List episodes for a show, fetch a single episode, and create, update, and delete episodes straight from the command line or an existing CMS. Episode creation accepts an audio file upload (MP3 recommended, up to 150 MB).

- **Human URL:** [https://developers.acast.com/](https://developers.acast.com/)
- **Base URL:** `https://api.acast.com`

#### Tags

- Episodes
- Publishing
- CMS

#### Properties

- [Documentation](https://developers.acast.com/)
- [API Reference](https://learn.acast.com/en/articles/5790019-acast-publishing-api)
- [OpenAPI](openapi/acast-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Acast Ad Markers API

Place or update ad markers within an episode via PATCH so dynamic ad insertion knows where to stitch pre-roll, mid-roll, and post-roll ads. Disabling monetization on a per-episode basis is not currently possible through the API.

- **Human URL:** [https://developers.acast.com/](https://developers.acast.com/)
- **Base URL:** `https://api.acast.com`

#### Tags

- Ad Markers
- Monetization
- Advertising

#### Properties

- [Documentation](https://developers.acast.com/)
- [API Reference](https://learn.acast.com/en/articles/5790019-acast-publishing-api)
- [OpenAPI](openapi/acast-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Acast Webhooks

Register HTTP callback URLs to receive real-time notifications when events occur on your account - for example when a new episode is published. Webhooks are server-to-endpoint HTTP callbacks, not a bidirectional or WebSocket transport.

- **Human URL:** [https://learn.acast.com/en/articles/3505461-what-is-a-webhook](https://learn.acast.com/en/articles/3505461-what-is-a-webhook)
- **Base URL:** `https://api.acast.com`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://learn.acast.com/en/articles/3505461-what-is-a-webhook)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/acast)
- [Website](https://www.acast.com)
- [Documentation](https://developers.acast.com/)
- [Plans](plans/acast-plans-pricing.yml)
- [Rate Limits](rate-limits/acast-rate-limits.yml)
- [Fin Ops](finops/acast-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
