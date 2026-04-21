# Architecture

> **This file is maintained automatically by the AI. Do not edit manually unless correcting an error. The only field you need to fill in is the Project Description below — the AI derives or grows everything else.**

> **Scope:** Fullstack project — a frontend and a backend application living alongside each other. Single source of truth for both sides, including the contract between them.

---

## Project Description

<!--
Paste a one-line or one-paragraph description of what you're building.
Example: "A task manager with a React web app and a Node REST API, for solo freelancers tracking client work."
The AI reads this on the first session and fills in Project + Applications below automatically.
-->

[PASTE PROJECT DESCRIPTION HERE]

---

## Project

_Auto-filled by the AI from the Project Description on the first session. The AI will confirm these with you before proceeding._

- **Name:** [Auto]
- **Type:** Fullstack [Auto — e.g. web app + REST API, mobile + GraphQL, SPA + gRPC]
- **Purpose:** [Auto — one line]
- **Target Users:** [Auto]
- **Stage:** [Auto] [e.g. prototype, MVP, beta, production]
- **Repo Layout:** [Auto] [e.g. monorepo with /frontend + /backend, separate folders, separate repos]

---

## Applications

_Auto-filled by the AI on the first session from the Project Description. Confirmed with the user before any scaffolding._

### Frontend
- **Location:** [Auto] [e.g. ./frontend, ./apps/web]
- **Kind:** [Auto] [e.g. SPA, SSR web, mobile, desktop]
- **Purpose:** [Auto — one line]

### Backend
- **Location:** [Auto] [e.g. ./backend, ./apps/api]
- **Kind:** [Auto] [e.g. REST API, GraphQL server, gRPC service, BFF]
- **Purpose:** [Auto — one line]

### Shared Code
- **Location:** [Auto or "none"] [e.g. ./shared, ./packages/types]
- **Contents:** [Auto] [e.g. shared types, validation schemas, lint config]

---

## Tech Stack

_Filled in as decisions are made. Each side has its own table because stacks diverge._

### Frontend
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

[e.g. Language | — | — | —]
[e.g. Framework | — | — | —]
[e.g. State | — | — | —]
[e.g. Styling | — | — | —]
[e.g. Build | — | — | —]

### Backend
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

[e.g. Language | — | — | —]
[e.g. Framework | — | — | —]
[e.g. Database | — | — | —]
[e.g. ORM/Query | — | — | —]
[e.g. Runtime | — | — | —]

### Shared / Tooling
| Layer | Choice | Version | Notes |
| ----- | ------ | ------- | ----- |

[e.g. Package manager | — | — | —]
[e.g. Monorepo tool | — | — | —]
[e.g. Lint / Format | — | — | —]

---

## Dependencies

_Tracked as packages are added. Keep in sync with lockfiles._

### Frontend
| Package | Purpose | Added |
| ------- | ------- | ----- |

### Backend
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

_Describe the end-to-end flow: browser/client → frontend → network → backend → data store. Note where auth, caching, and validation happen. A mermaid or ASCII diagram is welcome once there's enough to show._

---

## API Contract

_The interface between frontend and backend — the most important section of this file. Every shape the frontend depends on belongs here._

- **Protocol:** [Auto from description, e.g. REST+JSON, GraphQL, gRPC, WebSocket, mixed]
- **Base URL (dev):** [PLACEHOLDER]
- **Base URL (prod):** [PLACEHOLDER]
- **Versioning strategy:** [PLACEHOLDER] [e.g. URL prefix /v1, header, none-yet]
- **Schema source of truth:** [PLACEHOLDER] [e.g. OpenAPI file path, GraphQL schema, hand-written]

### Endpoints / Operations

| Path / Op | Method | Purpose | Request | Response | Auth | FE Callers | Added |
| --------- | ------ | ------- | ------- | -------- | ---- | ---------- | ----- |

### Real-time / Events

_If WebSockets, SSE, or pub/sub are used, list channels and event shapes here._

---

## Data Models

_Source-of-truth models. Note where each lives: backend-only, shared package, or frontend view model. Keep server models and UI models distinct — don't let one leak into the other._

---

## State Ownership

_What lives where. Prevents duplication and drift._

- **Server state** (source of truth in the backend): [PLACEHOLDER]
- **Client state** (ephemeral UI state): [PLACEHOLDER]
- **URL state** (shareable, bookmarkable): [PLACEHOLDER]
- **Local persistence** (cookies, localStorage, device storage): [PLACEHOLDER]

---

## Auth Flow

_How identity flows across the boundary. Fill in as auth is wired up._

- **Mechanism:** [PLACEHOLDER] [e.g. JWT, session cookies, OAuth, magic link]
- **Token storage (FE):** [PLACEHOLDER]
- **Token lifetime / refresh:** [PLACEHOLDER]
- **Logout semantics:** [PLACEHOLDER]
- **Protected route convention:** [PLACEHOLDER]

---

## Error Contract

_How errors are shaped server-side and handled client-side. A stable error shape prevents UI bugs on every new failure mode._

- **Error response shape:** [PLACEHOLDER — e.g. `{ code, message, details? }`]
- **HTTP status convention:** [PLACEHOLDER]
- **FE handling strategy:** [PLACEHOLDER — e.g. toast for 4xx, boundary for 5xx]
- **Correlation ID / tracing:** [PLACEHOLDER]

---

## Key Design Decisions

_Added as decisions are made. Tag each with its scope: [FE] / [BE] / [CONTRACT] / [INFRA] / [BOTH]._

---

## Environment Variables

_Never commit actual values. Mark which side consumes each._

### Frontend
| Variable | Purpose | Required | Default | Public? |
| -------- | ------- | -------- | ------- | ------- |

_(Public-to-the-browser vars need a prefix per your framework's convention; flag them here.)_

### Backend
| Variable | Purpose | Required | Default |
| -------- | ------- | -------- | ------- |

---

## External Integrations

_Added as services are connected. Note which side consumes each — some integrations belong on the server only (never expose their keys to the client)._

| Service | Consumed by | Purpose | Auth | Failure Mode |
| ------- | ----------- | ------- | ---- | ------------ |

---

## Testing Strategy

_Filled in as test infra is set up. Fullstack testing has more layers than single-app._

- **Frontend unit / component:** [PLACEHOLDER]
- **Backend unit:** [PLACEHOLDER]
- **Backend integration (DB, external services):** [PLACEHOLDER]
- **Contract tests (FE ↔ BE shape agreement):** [PLACEHOLDER]
- **End-to-end (browser driving real stack):** [PLACEHOLDER]
- **How to run each locally + in CI:** [PLACEHOLDER]

---

## Local Development

_How to bring the whole stack up on a dev machine. Should be copy-pasteable._

- **Prereqs:** [PLACEHOLDER]
- **First-time setup:** [PLACEHOLDER]
- **Run backend:** [PLACEHOLDER — port, command]
- **Run frontend:** [PLACEHOLDER — port, command]
- **Dev proxy / CORS:** [PLACEHOLDER]
- **Seed data / test accounts:** [PLACEHOLDER]

---

## Deployment & Infrastructure

_Filled in as deployment takes shape. Coordination matters here — a backend deploy can break production clients if the contract changes._

- **Frontend hosting:** [PLACEHOLDER]
- **Backend hosting:** [PLACEHOLDER]
- **Database / storage:** [PLACEHOLDER]
- **CI/CD pipelines:** [PLACEHOLDER]
- **Release coupling:** [PLACEHOLDER — are FE and BE shipped together, or independently?]
- **Backward-compat policy:** [PLACEHOLDER — how a BE change avoids breaking old FE clients still in the wild]
- **Secrets management:** [PLACEHOLDER]
- **Rollback plan:** [PLACEHOLDER]

---

## Technical Debt

_Added as shortcuts are taken. Tag with [FE] / [BE] / [CONTRACT] / [INFRA]._

- [ ]

---

## Known Bugs

_Added as bugs are discovered. Tag with [FE] / [BE] / [CONTRACT] / [INFRA]. Move to changelog when fixed._

- [ ]

---

## Out of Scope

_Added as things are explicitly deferred._

- [ ]

---

## Changelog

_Updated every session with a one-line summary. Always include a scope tag so it's obvious which side changed._

**Scope tags:** `[FE]` frontend · `[BE]` backend · `[CONTRACT]` API/shared types · `[BOTH]` coordinated change · `[INFRA]` deployment/tooling · `[DOCS]` documentation only

| Date | Scope | Change |
| ---- | ----- | ------ |
