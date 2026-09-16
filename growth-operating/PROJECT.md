# Growth Operating — project brief

For anyone picking up a task on this project, including a Cowork session starting
with no prior context. Read this first.

This file is **stable**: what the project is, how it works, what may and may not
be delegated. Current position — who is in the pipeline, what happens next — is
in `STATE.md` beside it, and changes constantly. Read both.

---

## What the business is

Josh builds and markets a digital product that a creator promotes to their own
audience. Revenue splits through Whop. He is the operator; the creator brings the
audience and the credibility.

His background is systems consultancy for companies — analysing a business's
systems and rebuilding them — plus marketing, finance and business management.

**Status: pre-revenue.** No creator signed, no message sent, no income.

## The one idea everything serves

**The gap:** the distance between what a creator's audience would willingly pay
for and what that creator currently offers them.

Size the gap and you have the deal. No gap, no deal, however good the creator
looks on every other measure. A large, engaged, trusting audience already being
sold exactly what it wants is not an opportunity — it is somebody else's finished
work.

**Route two is the operating mode:** partner with creators who already sell
something and grow it, rather than building from nothing for creators with no
product. The demand is proven by revenue before a message is sent.

## The niche

**Educators whose audience is owners** of salons, spas, med spas, barbershops,
gyms and studios. *Not* the businesses themselves.

That distinction is the whole thing. A salon posting transformations is
advertising to people who want a haircut — its followers are customers, not
buyers of a business education. Those accounts are the largest in the niche and
the most tempting, and they are worthless here.

## Where things live

| What | Where |
|---|---|
| Method: the gap, tiers, both gates, deal terms | `.claude/skills/growth-operating/SKILL.md` |
| Sourcing, Instagram search shapes, the query set, pre-screen bar | `.claude/skills/growth-operating/references/sourcing.md` |
| Outreach method, message structure, follow-up rule | `.claude/skills/growth-operating/references/outreach.md` |
| The cancelled toolchain, kept for its measured defects | `.claude/skills/growth-operating/references/monetise-stack.md` |
| Current position, live artifact URLs, open questions | `growth-operating/STATE.md` |
| Candidate handles and market proof | `growth-operating/vetting/` |
| The retired photography niche and why | `growth-operating/archive/photography/` |

Live artifacts (private, URLs in `STATE.md`): finance ledger, prospect register,
pricing audit, niche register.

---

## What can and cannot be delegated

**Read this before accepting any task.** The two worst outcomes on this project
have both been an agent reporting confidently on something it could not actually
see.

### Cannot be done by any agent

| Task | Why |
|---|---|
| Reading an Instagram, TikTok or YouTube profile | Blocked to unauthenticated fetches. Instagram returns HTTP 429, TikTok returns a title string, YouTube returns a footer |
| Follower counts, comment text, bio links, posting cadence | Not served. These are four of the six Gate 1 signals |
| Sending a DM or an email to a creator | Josh sends everything himself |
| Anything needing a login | Credentials are never handed to an assistant. Screenshots are the substitute |

If a task requires any of the above, **say so and stop.** Do not estimate, infer
from a creator's website, or fill the gap from general knowledge. The record
contains two confirmed cases of a tool under-reading a creator — once missing a
paid programme, once missing an entire education platform, a cohort course and a
podcast — and both produced wasted work downstream.

### Can be delegated

- **Market research by web search.** Finding productised incumbents in a segment,
  their price points, what their programmes cover.
- **Writing a pre-screen memo** from screenshots or notes Josh supplies.
- **Building a lead magnet** for a specific cleared creator, per `outreach.md`.
- **Adapting the pricing audit** to a creator's segment. The maths is
  niche-agnostic; `sourcing.md` lists the three changes needed.
- **Drafting an outreach message** against the four-part structure, once a memo
  exists.
- **Drafting deal terms** against the checklist in `SKILL.md`.
- **Reconciling a Whop payout** against the ledger.
- **Maintaining these files.**

---

## Standing rules

These are not preferences. Breaking one costs real money or real credibility.

1. **No memo, no outreach.** A written pre-screen memo exists before any message
   is sent. The register enforces it: nothing reaches Contacted without passing
   through Cleared.
2. **One follow-up, never two.** Four or five days after the first message, and
   it must add something rather than repeat the ask. Then stop. A third message
   converts nobody and costs the option of approaching again in six months.
3. **A named product is reliable when it appears; its absence proves nothing.**
   Always search a creator's name by hand before outreach — for a sales page, a
   podcast, a course platform, a professional body listing.
4. **Read every generated document end to end before it leaves Josh's hands.**
   Generated output has shipped with template markers, broken glyphs and repeated
   pull quotes inside otherwise finished work.
5. **Never fabricate a testimonial or an endorsement.** A generated endorsement is
   a misrepresentation, not a draft.
6. **Income claims are inherited.** If a creator advertises an earnings figure in
   their organic content, it becomes part of any offer built on it, and
   substantiating it becomes Josh's problem. Check before committing.
7. **Match the audience, not the craft.** Two people can do identical work and
   have completely different followers. Only an audience that pays to learn is a
   market.

## Conventions

- **Push straight to `main`.** No feature branches. Josh has deleted several
  stray branches and does not want more.
- **This repository is a public fork.** Anything committed is publicly readable.
  Purchased course material is read and summarised in conversation, then kept off
  the repo — the niche register artifact holds what needed keeping.
- **No credentials, ever.** Not for Whop, not for Instagram, not for anything.
- **Artifacts are private by default** and stay that way until Josh shares them.
  A creator's name or branding must not appear on an artifact URL until that
  creator has agreed.
- **Platform data comes from Josh**, as screenshots or pasted text.

## How to hand work back

State plainly what you did, what you could not do and why, and what you assumed.
If a screen or a search came back empty, say it came back empty — a negative
result is information, and a fabricated positive is worse than nothing.
