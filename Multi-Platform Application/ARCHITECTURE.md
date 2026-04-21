# Architecture

> **This file is maintained automatically by the AI. Do not edit manually unless correcting an error. The only field you need to fill in is the Project Description below — the AI derives or grows everything else.**

> **Scope:** Multi-app project. Any combination of backends and clients across platforms — web, Android, iOS, desktop, CLI, or server services. Apps may share a backend, share nothing but a repo, or anything in between.

---

## Project Description

<!--
Paste a one-line or one-paragraph description of what you're building, including which platforms you care about and how the apps relate to each other.
Example 1: "A note-taking product with a shared REST API, a React web app, and native iOS and Android clients — all backed by the same user accounts."
Example 2: "A monorepo holding three loosely related internal tools — a CLI, a web dashboard, and a Slack bot — all for the ops team."
Example 3: "A mobile-first shopping app (iOS + Android) with a backend API and an admin web panel."
The AI reads this on the first session and fills in Project + Applications below automatically.
-->

[PASTE PROJECT DESCRIPTION HERE]

---

## Project

_Auto-filled by the AI from the Project Description on the first session. Confirmed with the user before any work._

- **Name:** [Auto]
- **Type:** Multi-app / multi-platform
- **Purpose:** [Auto — one line]
- **Target Users:** [Auto]
- **Stage:** [Auto] [e.g. prototype, MVP, beta, production]
- **Repo Layout:** [Auto] [e.g. monorepo with /apps/*, polyrepo linked here, single folder with multiple entry points]
- **App Relationship Model:** [Auto] [e.g. "1 shared backend + N clients", "N independent apps sharing a design system", "siblings with no runtime coupling — shared repo only"]

---

## Applications

_Auto-filled on the first session from the Project Description. The AI maintains this table as apps are added, renamed, or retired._

### Summary

| App | Platform | Kind | Location | Uses | Status |
| --- | -------- | ---- | -------- | ---- | ------ |

<!--
Platform examples: web, android, ios, desktop, cli, server
Kind examples: REST API, GraphQL server, SPA, SSR web, native mobile, RN/Flutter mobile, Electron, Tauri, CLI tool, background worker
Uses column: names of other apps/services this app depends on at runtime (e.g. "api-server", "auth-service"). Empty if standalone.
Status: active / beta / experimental / deprecated
-->

### Per-App Detail

_One block per app. Added/removed as the suite evolves._

<!--
Template for each app:

### App: [name]
- **Platform:** [e.g. web, android, ios, desktop, cli, server]
- **Location:** [path in repo or repo URL]
- **Kind:** [framework/runtime]
- **Purpose:** [one line]
- **Runtime dependencies:** [which other apps/services it calls]
- **Platform constraints:** [e.g. iOS 15+, Android 7+, Chrome/Safari/Firefox, Node 20+]
- **Distribution:** [e.g. App Store, Play Store, own web hosting, npm, binary download]
- **Status:** [active / beta / deprecated]
-->

---

## Shared Code / Packages

_Code and assets used by more than one app. Kept here to prevent drift._

| Package | Location | Contents | Consumed By |
| ------- | -------- | -------- | ----------- |

[e.g. @project/types | ./shared/types | DTOs shared with the API | web, android, ios]
[e.g. @project/design | ./shared/design | tokens, icons, components | web, desktop]

---

## Tech Stack

_Filled in as decisions are made. Each app gets its own section — stacks diverge heavily across platforms._

### Backend / Services
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

### Web Client(s)
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

### Mobile (Android)
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

### Mobile (iOS)
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

### Desktop / CLI / Other
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

### Shared / Tooling
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

_Remove any sections that don't apply to this project._

---

## Dependencies

_Tracked as packages are added. One table per app/area so it's easy to see where weight sits._

### Backend / Services
| Package | Purpose | Added |
| ------- | ------- | ----- |

### Web
| Package | Purpose | Added |
| ------- | ------- | ----- |

### Android
| Package | Purpose | Added |
| ------- | ------- | ----- |

### iOS
| Package | Purpose | Added |
| ------- | ------- | ----- |

### Desktop / CLI / Other
| Package | Purpose | Added |
| ------- | ------- | ----- |

### Shared
| Package | Purpose | Added |
| ------- | ------- | ----- |

---

## File Structure

_Updated as files and directories are added._

```
.
```

---

## Architecture Overview

_How the apps fit together: who calls whom, where auth lives, where data lives, what's shared. Diagram welcome once there's enough to show. For independent apps in one repo, say that explicitly so future readers don't go looking for a shared architecture that isn't there._

---

## API Contracts

_One subsection per service. In a shared-backend setup there's usually one; in a service-oriented setup there may be many._

### Service: [Auto name]
- **Protocol:** [Auto] [e.g. REST+JSON, GraphQL, gRPC, WebSocket, mixed]
- **Base URL (dev):** [PLACEHOLDER]
- **Base URL (prod):** [PLACEHOLDER]
- **Versioning strategy:** [PLACEHOLDER] [e.g. URL prefix /v1, header, none-yet]
- **Schema source of truth:** [PLACEHOLDER] [e.g. OpenAPI file, GraphQL schema, proto files]
- **Backward-compat window:** [PLACEHOLDER — especially important if mobile clients are shipped to stores]

#### Endpoints / Operations

| Path / Op | Method | Purpose | Request | Response | Auth | Consumed By | Added |
| --------- | ------ | ------- | ------- | -------- | ---- | ----------- | ----- |

#### Real-time / Events

_WebSockets, SSE, push channels — list channel names and event shapes here._

_Add additional `### Service: …` blocks as more services are introduced._

---

## Client–API Usage Matrix

_Which client consumes which endpoint. Makes the blast radius of any API change instantly visible. Rebuilt as clients and endpoints evolve._

| Endpoint | Web | Android | iOS | Desktop | CLI | Other |
| -------- | :-: | :-----: | :-: | :-----: | :-: | :---: |

---

## Data Models

_Source-of-truth models. Note where each lives: server DB, shared package, or per-client view model. Keep server models and UI/local models distinct._

---

## State Ownership

_What lives where. With multiple clients this is critical — otherwise the same fact ends up in three places and drifts._

- **Server state** (authoritative, in the backend): [PLACEHOLDER]
- **Per-client cache** (e.g. React Query cache, Room DB, Core Data): [PLACEHOLDER]
- **Local-only state** (UI, ephemeral): [PLACEHOLDER]
- **Device persistence** (secure storage, prefs, cookies): [PLACEHOLDER]
- **Cross-device sync** (if any): [PLACEHOLDER]

---

## Auth Flow

_How identity flows. Platforms differ — OAuth redirects on web are different from mobile deep-link callbacks._

- **Mechanism:** [PLACEHOLDER] [e.g. JWT, session cookies, OAuth + PKCE, magic link, platform SSO]
- **Identity provider:** [PLACEHOLDER]
- **Web token storage:** [PLACEHOLDER]
- **Mobile token storage:** [PLACEHOLDER] [e.g. iOS Keychain, Android Keystore/EncryptedSharedPreferences]
- **Desktop token storage:** [PLACEHOLDER]
- **Refresh / expiry:** [PLACEHOLDER]
- **Logout semantics (per client):** [PLACEHOLDER]
- **Protected-route convention (per client):** [PLACEHOLDER]

---

## Error Contract

_Server-side error shape and how each client surfaces it. Consistent across clients unless noted._

- **Error response shape:** [PLACEHOLDER — e.g. `{ code, message, details? }`]
- **HTTP status convention:** [PLACEHOLDER]
- **Web handling strategy:** [PLACEHOLDER]
- **Mobile handling strategy:** [PLACEHOLDER — often differs, e.g. offline banners, retry queues]
- **Desktop / CLI handling:** [PLACEHOLDER]
- **Correlation ID / tracing:** [PLACEHOLDER]

---

## Cross-Cutting Concerns

_Platform-dependent features that need coordination. Filled in only if relevant to the project._

- **Push notifications:** [PLACEHOLDER — providers, per-platform setup, topic strategy]
- **Deep links / universal links:** [PLACEHOLDER — URL scheme, web-to-app handoff]
- **Offline support:** [PLACEHOLDER — which clients need it, sync model]
- **Browser support matrix:** [PLACEHOLDER — if web is in scope]
- **Accessibility:** [PLACEHOLDER — target standards per platform]
- **Internationalization:** [PLACEHOLDER — supported locales, source-of-truth catalog]
- **Analytics / telemetry:** [PLACEHOLDER — SDK, events schema, where data lands]
- **Feature flags:** [PLACEHOLDER — provider, scope (server vs per-client)]

---

## Key Design Decisions

_Added as decisions are made. Tag each with its scope — see the changelog scope-tag list below._

---

## Environment Variables

_Never commit actual values. Split by app so it's obvious what goes where. Public mobile/web bundles can be decompiled — never put secrets in them._

### Backend / Services
| Variable | Purpose | Required | Default |
| -------- | ------- | -------- | ------- |

### Web
| Variable | Purpose | Required | Default | Public? |
| -------- | ------- | -------- | ------- | ------- |

### Android
| Variable | Purpose | Required | Default | Public? |
| -------- | ------- | -------- | ------- | ------- |

### iOS
| Variable | Purpose | Required | Default | Public? |
| -------- | ------- | -------- | ------- | ------- |

### Desktop / CLI / Other
| Variable | Purpose | Required | Default |
| -------- | ------- | -------- | ------- |

---

## External Integrations

_Added as services are connected. "Consumed by" tells you the blast radius of an outage or key rotation._

| Service | Consumed By | Purpose | Auth | Failure Mode |
| ------- | ----------- | ------- | ---- | ------------ |

---

## Testing Strategy

_Multi-app testing has more layers than single- or fullstack-app. Fill in as infrastructure is set up._

- **Backend unit:** [PLACEHOLDER]
- **Backend integration (DB, external services):** [PLACEHOLDER]
- **Web unit / component:** [PLACEHOLDER]
- **Android unit / instrumentation:** [PLACEHOLDER]
- **iOS unit / UI tests:** [PLACEHOLDER]
- **Desktop / CLI:** [PLACEHOLDER]
- **Shared-package unit:** [PLACEHOLDER]
- **Contract tests (clients ↔ API):** [PLACEHOLDER]
- **End-to-end per client:** [PLACEHOLDER — which user journeys, which clients]
- **How to run each locally and in CI:** [PLACEHOLDER]

---

## Local Development

_How to bring any subset of the suite up on a dev machine. Should be copy-pasteable per app._

- **Prereqs:** [PLACEHOLDER]
- **First-time setup:** [PLACEHOLDER]
- **Run backend / services:** [PLACEHOLDER]
- **Run web:** [PLACEHOLDER]
- **Run Android:** [PLACEHOLDER]
- **Run iOS:** [PLACEHOLDER]
- **Run desktop / CLI / other:** [PLACEHOLDER]
- **Dev proxy / CORS / device network config:** [PLACEHOLDER]
- **Seed data / test accounts:** [PLACEHOLDER]

---

## Deployment & Distribution

_Each platform distributes differently. Coordination matters — a backend change can break a mobile app that's already in thousands of pockets._

- **Backend hosting:** [PLACEHOLDER]
- **Database / storage:** [PLACEHOLDER]
- **Web hosting / CDN:** [PLACEHOLDER]
- **Android distribution:** [PLACEHOLDER — Play Store, internal track, APK]
- **iOS distribution:** [PLACEHOLDER — App Store, TestFlight, enterprise]
- **Desktop distribution:** [PLACEHOLDER — installers, auto-update channel, code-signing]
- **CLI distribution:** [PLACEHOLDER — npm, Homebrew, binary release]
- **CI/CD pipelines:** [PLACEHOLDER]
- **Release cadence per app:** [PLACEHOLDER]
- **Release coupling:** [PLACEHOLDER — which apps ship together, which independently]
- **Backward-compat policy:** [PLACEHOLDER — especially how the backend supports old mobile versions still in the wild]
- **Forced-upgrade strategy (mobile):** [PLACEHOLDER — minimum supported version, upgrade prompt]
- **Secrets management:** [PLACEHOLDER]
- **Rollback plan per app:** [PLACEHOLDER]

---

## Technical Debt

_Added as shortcuts are taken. Tag with the relevant scope tag(s) from the changelog legend below._

- [ ]

---

## Known Bugs

_Added as bugs are discovered. Tag with scope. Move to changelog when fixed._

- [ ]

---

## Out of Scope

_Added as things are explicitly deferred._

- [ ]

---

## Changelog

_Updated every session with a one-line summary. Always include one or more scope tags._

**Scope tag legend** _(the AI updates this list during bootstrap to match the actual apps in this project):_

- `[API]` backend / service
- `[WEB]` web client
- `[AND]` Android client
- `[IOS]` iOS client
- `[DESK]` desktop client
- `[CLI]` CLI client
- `[SHARED]` code consumed by multiple apps (types, design system, utils)
- `[CONTRACT]` API contract change (affects one or more clients)
- `[INFRA]` CI, deployment, tooling
- `[DOCS]` documentation only
- `[ALL]` touches every app in the suite

| Date | Scope | Change |
| ---- | ----- | ------ |
