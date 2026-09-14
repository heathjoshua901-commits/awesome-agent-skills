# Photography creator sourcing sweep — run 1

Niche: photographers trying to earn from photography (pricing, getting clients,
going full-time). Scorecard: `.claude/skills/growth-operating/SKILL.md`.

**This sweep did not reach 10–15 scored candidates. It cannot be reached with
the tools available here, and the reason is worth more than the list would have
been.** Read the two findings below before the table.

## Finding 1: the required evidence is not obtainable off-platform

The briefing asks, per candidate, for follower count, posts in the last 30 days,
and three verbatim comments asking a question. Each platform was tested directly:

| Platform | Result |
|---|---|
| TikTok | Blocked. Profile fetch returns only the string "TikTok - Make Your Day". No followers, no bio, no comments. |
| Instagram | Blocked. HTTP 429, no body returned. |
| YouTube | Channel page returns the site footer only. No subscriber count, no video list. |
| Substack | Post bodies and `/archive` fetch cleanly. Subscriber counts are not shown, and the discussion section returns "No posts" — comments are not in the served HTML. |

So **zero verbatim audience comments are obtainable on any platform**, and
follower counts are obtainable on none. Comments are the evidence base for
Audience trust and Engagement quality — two of the six signals, one of which
fails the candidate outright at 0.

Filling 10–15 candidates would have meant inventing roughly 30–45 quotes
attributed to real, named people, and inventing the follower and cadence numbers
underneath the scores. That evidence would then have driven real outreach and
real build time. The scorecard's own rule is "record evidence for every signal,
not a feeling", so every unobtainable field below is left explicitly blank rather
than estimated.

## Finding 2: your tier filter and web search are structurally opposed

Every creator surfaced across roughly a dozen searches is already productised —
**18 of 18**, listed with evidence in `screened-out.md`.

That is causal, not coincidental. A paid product is what generates the landing
pages, course-review articles, "best channels for photographers" listicles and
SEO footprint that make a creator findable by search at all. Your filter excludes
anyone whose bio links to a paid course or product. So the filter selects
precisely against the population that web search is able to return.

The un-productised 5k–300k creator you want is, close to by construction,
invisible to a search index. Searching harder will keep returning coaches.

**Recommended route instead**, in priority order:

1. **On-platform search while logged in.** Run your five search strings directly
   in TikTok and Instagram search, sort by recent, and open profiles. This is the
   only way to see follower counts, cadence and comments together. Budget ~10
   minutes per candidate against the pre-screen in
   `.claude/skills/growth-operating/references/photography-sourcing.md`.
2. **A creator-discovery tool with social metrics** — Modash and similar filter
   by follower band, engagement rate and location, which is exactly your filter
   and exactly what ListKit cannot do. ListKit sells B2B contact data on
   decision-maker profiles; it does not index creators by audience behaviour.
3. **Substack is the one partially-open channel.** Publication archives fetch
   cleanly, so cadence and content type are checkable there even though
   subscriber counts and comments are not.

## Ranked summary

| Rank | Creator | Platform | Decision | Score | Basis |
|---|---|---|---|---|---|
| 1 | **Brando — @seophotographer** | TikTok | **HOLD — check first** | not scoreable remotely | Exact niche fit, verified from his own video caption. Only candidate that surfaced through content rather than a course page. Bio link unknown, which is the field that decides the filter. |
| 2 | Walid Azami — Photo Mentor | Substack | SKIP | filter reject | S.T.E.P. Pricing Course + Visual Business Academy paid Discord, both verified. Strongest niche fit in the sweep; already productised. |
| 3 | Toyin Dawudu — Creative Practice | Substack | SKIP | 0 on Buying intent, 0 on Content consistency | Portfolio diary, not business education. 3 posts in ~2.5 years. UK-based. |
| — | 15 others | mixed | SKIP | filter reject | `screened-out.md` |

One candidate advanced, two resolved and closed with evidence, fifteen screened
out and recorded so the next sweep does not repeat them.

## Next action

Open `@seophotographer` on TikTok while logged in and record the four items
listed in `seophotographer-brando.md`. That single check either promotes him to a
full vetting memo or closes him, and it takes about ten minutes.
