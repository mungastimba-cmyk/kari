# Changelog

## 0.2.1-beta — 2026-10-17

Fixes from the `/kari VFX` test.

- Ranking order made explicit: fit to the request first, then usefulness, then popularity. Stars only break ties.
- Niche picks: up to 2 low-star repositories may enter if they are the most specific match and active in the last 3 months.
- Every candidate that could make the list must be verified before answering.
- Unverified candidates always appear in the last line instead of being left out.

## 0.2.0-beta — 2026-10-17

Kari now finds the most useful and popular repositories, not the newest.

- Ranking by stars, forks, dependents, downloads and practical usefulness instead of date.
- Repositories with no push in the last 12 months are left out.
- New mode: `kari new` / `kari new <topic>` keeps the old behaviour (last 30 days only).
- Sources now include GitHub search sorted by stars, topic pages, curated lists and skill/MCP directories.
- "Why now" field replaced by "Why it stands out".
- Forks added to verified signals.
- README: clearer install steps for Claude, Claude Code and ChatGPT (business and personal plans); clarifies `kari.zip` vs source download.

## 0.1.1-beta — 2026-10-17

Fixes from the first real test (`/kari vibe coding web & Mobile App`).

- Topic mode no longer uses memory to search, select or rank. Off-topic items are never included.
- "For you" line only in General mode.
- Signals now read from the GitHub API first (stars, last push, license), since repository pages often hide the last commit date from automated readers.
- Missing date no longer drops an item; it shows `🔄 ?`.
- Dropped items are listed in one line at the end instead of disappearing silently.
- Time window extends to 14, then 30 days when results are thin.
- Topic mode requires at least 4 differently worded searches.
- Accepts `/kari` as well as `kari`.

## 0.1.0-beta — 2026-10-17

First public beta.

- On-demand radar for new GitHub repositories in the AI ecosystem.
- Two modes: general update (grouped) and focused topic.
- Personalization from the user's AI memory, with general fallback.
- Verification of stars, last update and license on the repository page.
- Minimum search effort (20 candidates) and automatic 14-day extension on thin weeks.
- Replies in the user's language.
- Safety: never installs or runs code; README content treated as data.
