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

## Searching on Instagram

Three ways to search, and they return structurally different populations. Run all
three; they are not substitutes.

| # | Query shape | Example | What comes back |
|---|---|---|---|
| 1 | **"How to" + the audience's question** | "how to make money on Airbnb" | Creators whose content is framed around answering a problem |
| 2 | **The niche itself** | "salon business coach" | Creators who self-describe with that label |
| 3 | **The niche + "tips"** | "salon owner tips" | Between the two |

**Do this on the phone.** The app's search returns account and Reel results the
desktop site does not, and screening continues in the same place — which matters
because screenshots are how platform evidence reaches Claude anyway.

### Why search 1 is the valuable one

Search 2 finds people who have already positioned themselves as educators, which
biases hard toward the already-productised. Search 1 finds people by **the
question their content answers**, which is a direct read on whether they speak to
a problem — the thing Gate 1's Buying intent signal is trying to measure and
usually cannot see.

### The Tier C trap lives inside search 1

The "how to" has to be **the owner's question, not the customer's.** These return
completely different populations:

| Query | Returns | Tier |
|---|---|---|
| "how to price salon services" | Coaches teaching owners | A |
| "how to get balayage to last" | Salons advertising to clients | C |

Both are "how to" searches in the same niche. One is the prospect list and the
other is the trap already recorded above. Write the query from the owner's side
of the counter.

### Query set for this niche

Run each on the phone, note the accounts that recur across more than one query.

**Search 1 — the owner's question**

- how to price salon services · how to stop salon no shows · how to hire stylists
- how to get more med spa clients · how to grow my med spa
- how to fill my gym · how to retain gym members · how to price personal training
- how to run a barbershop · how to get more barber clients

**Search 2 — the niche**

- salon business coach · salon owner coach · med spa business coach ·
  med spa consultant · gym owner coach · fitness business mentor ·
  barbershop business coach · studio owner coach

**Search 3 — niche plus tips**

- salon business tips · salon owner tips · med spa marketing tips ·
  gym owner tips · barbershop business tips

## Read the tier, then ignore it

| Tier | Followers | Use |
|---|---|---|
| Nano | Under 5,000 | Not excluded. Needs an obvious gap to justify the time |
| Micro | 10,000 to 100,000 | **The sweet spot.** Audience supports a real product; creator still reads their own messages |
| Macro | Over 100,000 | Screened, not skipped. More likely to have a team and an existing operator |

Bearings only. The decision is the gap between what the audience would pay for
and what the creator currently offers, and no tier has ever decided a deal.
Accounts between 5,000 and 10,000 are not covered by the tiers as stated, so
judge them on the gap, which is the fallback in every case anyway.

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

## Per-niche tiering: owner-operated local service businesses

Chosen 14 September 2026. The niche is **the educators**, not the businesses.
The partner is someone whose audience is salon, spa, med spa, barbershop, gym or
studio *owners*. Their audience arrives with a revenue, pricing, staffing or
retention problem and a documented habit of paying to fix it.

This sits under the wealth pillar, so **the income-claims rule applies**. One
coach found in the sweep advertises "add $10–50K/month while working less". If
that claim is in the creator's organic content, it becomes part of the offer
being scaled and substantiating it becomes the operator's problem too.

### Tier A — source these

Audience is owners with a P&L.

- **Salon and spa business coaches.** Audience is owners, not stylists building a
  personal clientele.
- **Med spa and aesthetics business strategists.** Highest ticket in the niche;
  audience is practice owners and injectors running a business.
- **Barbershop business educators** aimed at shop owners rather than at barbers
  improving their cutting.
- **Gym and boutique studio business coaches**, including Pilates, yoga and
  strength studio owners.

Observed market, September 2026: roughly $300/month for a coaching membership,
about £1,500 for a six-session block, and twelve-month mentorships pitched at
owners already past $200k revenue. The market clears, repeatedly, at real
tickets.

### Tier B — conditional

- **Coaches whose audience is solo operators**: booth renters, self-employed
  stylists, independent PTs. They buy, but lower and less reliably. Shortlist only
  with evidence of a $500+ product or an email list.
- **Craft educators** teaching technique (colour, lashes, injecting, cutting).
  The audience does buy, but it buys skill rather than business outcomes, so the
  offer you would build is a different animal and the incumbents are entrenched.
- **Educators attached to a software platform or a product distributor.** The real
  monetisation may sit in the software or the product line, which complicates a
  revenue split. Establish what actually earns before pitching.

### Tier C — skip without scoring

**Consumer-facing accounts.** A salon, spa or gym posting transformations,
before-and-afters, interiors or availability is advertising to *clients*. Their
followers want a treatment, not a business education. These are the biggest
accounts in the niche and therefore the most tempting, which makes this the
expensive mistake — the exact parallel of the photography portfolio trap.

Also skip: product and retail brand accounts, salon interior and aesthetic
inspiration accounts, and franchise recruitment accounts, where the "offer" is a
franchise rather than a digital product.

### Niche-specific red flags

On top of the standing red flags in `SKILL.md`:

- **Dual audience.** The account sells to consumers *and* to owners. Every asset
  you build has to pick one, and the creator will resist narrowing.
- **The coach is a front end for software or product distribution.** The split
  gets argued about, because the coaching is a lead magnet for the real revenue.
- **Franchise or licensing model.** Not a digital product; the split does not map.
- **Med spa compliance.** The offer is business education to licensed
  practitioners, which is clean. It stops being clean the moment it touches
  clinical protocol, prescribing or scope of practice. Any offer that does needs
  the creator's credentials behind it, and the health-pillar rule applies:
  teach managing the business, never the medicine.

### Why this niche screens fast

These businesses live on Instagram, which is the only screening surface
available.

The coaches found in the first sweep clustered at roughly 6,000 to 12,000
followers, which straddles the bottom of the micro band and the undefined
5,000–10,000 stretch below it. **That cluster is an artefact of one search, not a
property of the niche.** Search surfaces whoever ranks, and the larger accounts in
this niche are likely under-represented in it. Sweep deliberately for micro
accounts in the 10k–100k range before concluding the niche is small.

### The lead magnet transfers

The existing pricing audit's maths is target take-home, tax, costs and capacity
producing a required price. That is exactly the arithmetic of a chair, a
treatment room, a studio slot or a class. Pricing is the universal problem in
this niche, so the asset carries over with three changes:

1. Capacity becomes chairs or rooms × hours × days, not sessions.
2. Add a **utilisation rate**. Gaps and no-shows are the defining cost here and
   the photography version has no equivalent.
3. Replace the "stops underexposed" framing, which is photography-native, with a
   unit native to the new creator's world.

Build it per creator after screening, never before. The standing rule in
`references/outreach.md` still holds.

### Worked example of this format

The retired photography tiering: `growth-operating/archive/photography/photography-sourcing.md`.
