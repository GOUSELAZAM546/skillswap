# SkillSwap — Creator Opportunity Engine

> Turn your skills into the right opportunities.

SkillSwap is a creator marketplace where users can discover creators, request services, and manage project requests, while creators can offer services and manage incoming projects.

## Hackathon Information

- Hackathon: Code2Career AI Hackathon
- Hackathon ID: AZIS-WBR57N
- Track: Track 2 — Web Product
- Brief: SkillSwap — Creator Economy / Creator Gig Marketplace

## Features

### 1. Offer a Service
Creators can publish a service with:
- Title
- Category
- Rate
- Required experience
- Availability
- Description

### 2. Browse, Search and Filter
Users can:
- Browse creator services
- Search services
- Filter by category
- Sort and discover relevant services
- View "Why this match?" information

### 3. Request a Service
Users can request a creator service and receive a confirmation.

Requests begin with:

`Pending`

### 4. Creator Requests
Creators can view incoming project requests and:

- Accept
- Decline

Accepted requests move to projects.

### 5. My Project Requests
Users can track requests as:

- Pending
- Accepted
- Declined

## Decision Points

### DP1 — Rejection Behavior

When a creator declines a request, the request becomes `Declined`.

The user can then explore similar services instead of being left at a dead end.

### DP2 — Double Booking

A service with an active `Pending` or `Accepted` request cannot receive another active request.

This prevents duplicate active bookings for the same service.

### DP3 — Discovery and Ranking

SkillSwap uses an explainable relevance calculation for service discovery.

The current weighting considers skill relevance, category relevance, experience, availability, and recency.

## Matching Logic

| Signal | Weight |
|---|---:|
| Skill relevance | 50% |
| Category relevance | 20% |
| Experience | 15% |
| Availability | 10% |
| Recency | 5% |

The application can show a relevance score and explain why a service matches.

## Project Workspace

After a project is accepted, the creator and user can use the Project Workspace.

Project flow:

`Accepted → In Progress → Completed → Review`

The workspace includes:

- Project requirements
- Deliverables
- Deadline
- Project status
- Review and rating

## Technology

- HTML5
- CSS3
- JavaScript
- Browser LocalStorage

The application is currently implemented as a client-side web application.

## Authentication

Authentication is not implemented.

There is no login or signup requirement. All application features can be accessed directly through the interface.

## Data Storage

The current prototype uses browser LocalStorage for:

- Creator profiles
- Services
- Project requests
- Booking statuses
- Project workspace data
- Reviews

## Standard API

**Standard API: Not implemented.**

The application uses HTML, CSS and JavaScript with browser LocalStorage for persistence.

All five required features are accessible through the browser UI.

## How to Run

1. Clone or download this repository.
2. Open the project in VS Code.
3. Open the HTML file.
4. Run it using VS Code Live Server.
5. Open the displayed local URL in a browser.

## Project Structure

```text
skillswap/
├── skillswap1.html
├── README.md
└── DECISIONS.md
