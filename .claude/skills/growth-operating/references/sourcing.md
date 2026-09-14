# Sourcing and pre-screen

Stage 1 and the front half of stage 2. Niche-agnostic: the method below holds
whatever niche is being worked. The per-niche tiering gets filled in once a niche
is chosen.

## ListKit does not find creators

**Discovery is on-platform.** ListKit sells triple-verified B2B contact data on
decision-maker profiles. It can enrich and hold a creator record once you have a
name, but it does not index creators by comment quality or audience behaviour,
which is what Gate 1 actually scores.

Find candidates by searching the platform the creator posts on, then push the
record into ListKit for contact data and pipeline tracking. Treat it as a CRM,
not as a source.

## Sort by whose audience it is, before scoring anything

Follower count is usually the least informative number on the page. What matters
is whether the audience is made of people with the problem and the money, or
people who enjoy the content.

Every niche splits three ways. Tier it before spending a screen on it.

| Tier | Test | Action |
|---|---|---|
| **A** | The audience is operators with a revenue or outcome problem, and the niche already clears real money | Source these |
| **B** | The audience has bought something, but only at a low ticket, or buying evidence is thin | Shortlist only with evidence of a higher-priced sale or an email list |
| **C** | The audience consumes: enthusiasts, admirers, inspiration, news, gear | **Skip without scoring.** They score 0 on Buying intent, which fails Gate 1 outright no matter how large the following |

The Tier C trap is the expensive one, because those accounts are usually the
biggest and therefore the most tempting.

## Gate 1 cannot be completed at stage 1

Only four of the six signals are visible before the creator replies.

| Gate 1 signal | Visible pre-contact | Where to look |
|---|---|---|
| Audience trust | Partly | Do commenters ask the creator questions, and does the creator answer? |
| Buying intent in niche | Yes | Tier above, plus what the comments ask about |
| Engagement quality | Yes | Comments on the last 20 posts |
| Existing monetisation | Yes | Bio links: Whop, Gumroad, Kajabi, Teachable, Skool, a newsletter signup |
| Responsiveness | No | Only after you message them |
| Content consistency | Yes | Posting cadence over the last 6 months |

The skill's pass bar is 8 of 12. Four observable signals cap out at 8, so **a
public-data pass is not possible and must not be faked.**

**Pre-screen bar:** score the four observable signals out of 8. Shortlist at 5 or
more with no 0 on Audience trust or Buying intent. Complete the full 12-point
score after the first reply. Responsiveness is unscoreable until they respond,
and it is the signal that eliminates most otherwise-strong candidates.

## Per-candidate pre-screen, about 10 minutes

1. Tier check. Tier C is dropped without scoring.
2. Read the comments on the last 20 posts. Record two verbatim comments that name
   a problem. If there are none, Engagement quality is 0.
3. Open every bio link. Note any existing product and its price.
4. Check posting cadence across 6 months.
5. Write the memo. No memo, no stage 3 — the skill's standing rule.

### Pre-screen memo

```
Creator:
Platform and handle:
Tier: A / B / C
Pre-screen score: X/8   (Audience trust, Buying intent, Engagement quality, Existing monetisation)
Evidence per signal:
Two verbatim audience comments:
Existing product and price:
Red flags:
Decision: contact / skip
The one problem their audience keeps asking about:
```

Carry this into the full vetting memo in `SKILL.md` once they reply.

## What Claude cannot see

Tested directly from a cloud session, with full network access:

| Platform | Result |
|---|---|
| TikTok | Blocked. Profile fetch returns only the string "TikTok - Make Your Day" |
| Instagram | Blocked. HTTP 429, no body |
| YouTube | Channel page returns the site footer only. No subscriber count, no video list |
| Substack | Post bodies and `/archive` fetch cleanly. Subscriber counts are not shown, and comments are not in the served HTML |

So **zero verbatim audience comments are obtainable by Claude on any platform**,
and follower counts on none. Comments are the evidence base for two of the six
signals, one of which fails a candidate outright at 0.

All platform data comes from the operator: screenshots, or pasted text. Web
search reaches sales pages, podcasts and press, which is how a creator's
*products* get verified — never their audience.

## The tool under-reads, twice confirmed

The platform analysis is built on a fixed, small post sample. Twice it has
reported a creator as having no product or one product when a manual search found
substantially more, including a full education platform in one case.

**A named product is reliable when it appears. Its absence proves nothing.** Use
the tool to confirm, never to clear. Before any outreach, search the creator's
name directly for a sales page, a podcast, a course platform and any professional
body listing.

## Per-niche tiering

Not yet filled. Once a niche is chosen, this section gets the Tier A / B / C
split for that niche, its typical price points, and its niche-specific red flags.

Archived photography tiering, kept as a worked example of the format:
`growth-operating/archive/photography/photography-sourcing.md`.
