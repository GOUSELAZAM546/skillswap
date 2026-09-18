# SkillSwap — Decision Points

## Decision Point 1 — Rejection Behavior

When a creator declines a project request, SkillSwap changes the request status to `Declined`.

The user can then explore similar services in the same category, so the rejection does not leave the user without a next action.

## Decision Point 2 — Double Booking

SkillSwap prevents a new active request for a service when that service already has a `Pending` or `Accepted` request.

This keeps the booking state clear and prevents multiple active requests for the same service.

## Decision Point 3 — Discovery / Ranking

SkillSwap uses an explainable relevance calculation instead of an unexplained ranking.

The matching logic considers skill relevance, category relevance, experience, availability, and recency, allowing the interface to explain why a service is considered relevant.
