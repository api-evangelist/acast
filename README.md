# Acast (acast)

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
