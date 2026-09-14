# Growth Operating: where things stand

Session handover. Read this first, then `.claude/skills/growth-operating/SKILL.md`.

Last updated: 14 September 2026.

## The business

Josh builds and markets a digital product that a creator promotes. Revenue is
split through Whop. Josh's background is systems consultancy, marketing, finance
and photography, which is why photography became the niche.

## Live assets

| Asset | Where |
|---|---|
| Finance ledger | https://claude.ai/code/artifact/01c7de1c-82ce-484a-8255-6d161092ea1e |
| Pricing audit, built for the Rhea Whitney approach | https://claude.ai/code/artifact/20b78698-0bd4-4262-8e82-d3e66bbfecf5 |

The ledger is connected to its shared database and holds the settings, one
example creator, one example sale and two example expense rows. Split is set to
50/50 on both the default and the example creator.

The pricing audit is unbranded and its call to action points at a placeholder.
It must not carry a creator's name until that creator agrees.

## Decisions made

- **Split is 50/50** at the start. A different percentage gets communicated later
  if it changes.
- **Route two, not route one.** Partner with creators who already sell something
  and grow it, rather than building for creators with nothing. Reasoning is in
  the skill under "Why route one is structurally hard": six screened creators
  produced no route-one candidate, and an un-productised learning audience is an
  unstable state that closes itself.
- **Both repositories push straight to main.** No feature branches. Josh deleted
  several stray branches and does not want more.
- **Documentation of the Monetise tools covers what they take and return**, never
  the course material itself, because the purchase may be refunded.

## Open questions

| Question | Why it matters |
|---|---|
| Does Whop split gross or net of fees? | The ledger assumes the split applies **after** Whop's fees. If Whop splits gross, the creator's share will not match the ledger. Compare on the first real payout and tell Claude which basis was used |
| Whop's real fee rates | The three rates in the ledger's settings are industry assumptions, not verified. Published sources disagree on whether a 3% platform fee still exists. Read them off a real payout |
| Does the split cover bumps and upsells? | Not stated in any agreement yet. Both readings are defensible, which is why it has to be written down before launch |
| Is bundled Synthesise AI perpetual? | Standalone is $2,999 one-time. If the bundled version expires with the programme, the comparison changes |

## The Monetise subscription

Bought 8 September 2026, $1,995 over twelve monthly instalments of $166.25
through Splitit. A refund was requested by email on 14 September and support
agreed to process it. **Status at last update: requested, not yet confirmed.**

If the refund completes, access to Synthesise AI, Ghostwriter OS and the funnel
mapper ends. Everything worth keeping from those tools is already recorded in
`references/monetise-stack.md`.

The one tool that does something this session cannot: Synthesise AI reads a
creator's Instagram and YouTube directly. Instagram, TikTok and YouTube serve
nothing to an unauthenticated fetch, so all platform screening has to be done by
Josh regardless of which tools he keeps.

## Pipeline position

Nothing has been sent. No creator has been signed. No revenue exists.

Six creators screened, all failed. Four already productised, two with audiences
that do not pay to learn. Details in `vetting/screening-queue.md`.

**The current candidate is `@rheawhitney`.** Nineteen thousand followers, a
data-driven pricing specialism, one directly promoted training. The only free
asset she has ever offered was a workbook at a webinar about a year ago, which
ran once and stopped.

The outreach angle: she built a free step once and switched it off. The pricing
audit is the evergreen version of it.

## Immediate next actions

1. Confirm the webinar workbook is not still linked anywhere permanent. If it is,
   the outreach message's second paragraph is wrong and needs rewriting.
2. Establish her baseline: training name, price, what it covers, how she sells it.
3. Put her training name and link into the pricing audit, swap the accent token
   to her brand colour, then share the artifact.
4. Send the outreach message. The draft and its rules are in
   `references/outreach.md`.
5. Once a payout exists, reconcile it against the ledger and settle the gross or
   net question above.

## Working notes

- Claude cannot read Instagram, TikTok, YouTube or Substack from a cloud session.
  Platform data always comes from Josh.
- Screenshots are the fastest way to hand Claude interface detail. Never
  credentials.
- Every generated document gets read end to end before it leaves Josh's hands.
  The Monetise generator leaks template markers and duplicate pull quotes into
  otherwise finished output.
