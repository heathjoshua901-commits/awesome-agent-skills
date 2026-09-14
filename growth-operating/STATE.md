# Growth Operating: where things stand

Session handover. Read this first, then `.claude/skills/growth-operating/SKILL.md`.

Last updated: 14 September 2026.

## The business

Josh builds and markets a digital product that a creator promotes. Revenue is
split through Whop. Josh's background is systems consultancy for companies
(analysing a business's systems and rebuilding them), plus marketing, finance and
business management. He also knows photography well.

## Live assets

| Asset | Where |
|---|---|
| Finance ledger | https://claude.ai/code/artifact/01c7de1c-82ce-484a-8255-6d161092ea1e |
| Pricing audit, unbranded, built for a capacity-constrained service business | https://claude.ai/code/artifact/20b78698-0bd4-4262-8e82-d3e66bbfecf5 |
| Niche register, private, holds the prospecting list kept off this repo | https://claude.ai/code/artifact/f755ee23-4524-4496-9bdf-c16326d82d09 |

The ledger is connected to its shared database and holds the settings, one
example creator, one example sale and two example expense rows. Split is set to
50/50 on both the default and the example creator.

The pricing audit is unbranded and its call to action points at a placeholder.
It must not carry a creator's name until that creator agrees. **It was built for
photography but the maths is niche-agnostic**: target take-home, tax, costs and
capacity produce a required price per session. It transfers unchanged to any
capacity-constrained service business, which is worth weighing in the niche
choice. Only the "stops underexposed" framing is photography-specific.

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
  the course material itself, because the purchase may be refunded and because
  this repository is a public fork. Course documents are read and summarised in
  conversation, then kept off the repo.

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

**The photography niche was retired on 14 September.** Six creators screened,
none passed. The full record, the tiering and the vetting memos are in
`growth-operating/archive/photography/`, which has a README explaining the
retirement and what survived into the live skill.

`@rheawhitney` was the standing candidate and is archived with the rest. If the
niche is ever revisited, that is where to restart.

## The niche switch, 14 September

**Decided: switch. Niche to be chosen by Josh.**

The reasoning. The programme's prospecting material selects niches on **demand**:
an audience that arrives already carrying a problem it wants gone. Photography
appears nowhere in it, under any heading. Photography was chosen on **Josh's
expertise** instead, and six screens with no pass is what that difference looks
like in practice.

The replacement must be chosen on demand, not on familiarity, or the same error
repeats. Three constraints on the choice, in this order:

1. **Does the audience arrive with a problem it wants gone?** Non-negotiable.
   Interest is not intent.
2. **Can it be screened from outside?** Josh's screening surface is Instagram.
   Niches whose creators live on Facebook, LinkedIn or YouTube screen far more
   slowly, because Gate 1 needs comment sections.
3. **Does Josh's background let him build the offer?** Third, not first. This is
   the constraint that went first last time.

The full niche list is in the private register artifact above. The entries
flagged "fit" there map to systems consultancy, finance and business management.

**Carried forward regardless of niche:** the two gates, the outreach method, the
productised-peer sourcing rule, the tier-before-scoring rule, the 8-point
pre-screen cap, and the pricing-audit maths.

## Immediate next actions

1. **Josh chooses the niche.** Nothing below can start until then.
2. Fill the per-niche tiering section at the end of `references/sourcing.md`:
   Tier A / B / C for the new niche, its price points, its niche-specific red
   flags.
3. Build a fresh screening queue of handles in the new niche.
4. Decide whether the pricing audit is reusable as the new niche's lead magnet or
   whether a different asset is needed.
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
- The platform analysis has under-read a creator's product range twice. A named
  product is reliable when it appears; its absence proves nothing. Always search
  the creator's name by hand before outreach.
