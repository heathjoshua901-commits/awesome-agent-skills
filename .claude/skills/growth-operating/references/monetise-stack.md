# Monetise stack: what each tool takes and returns

Operational notes on the tools inside Monetise, kept so their useful behaviour
can be reproduced without the software. Recorded because access ends if the
refund completes.

For each tool: what you feed it, what it returns, and which pipeline stage it
serves. Stage numbers refer to the table in `SKILL.md`.

---

## Ghostwriter OS — Campaign DNA

**Stages served:** 3 (outreach) and 7 (launch assets).

Campaign DNA is reusable context fed to the copy agents, so the same brand,
audience and offer facts are not retyped per run. It is a context-management
layer, not a generator.

### Structure

Three independent module types. Each holds four fields.

| Module | Question it answers |
|---|---|
| Personality | Who is speaking: brand, tone of voice, credentials |
| Audience | Who is being spoken to: ideal customer, beliefs, pain points |
| Product | What is being offered: offer, problem solved, solution |

**Field names are not recorded.** Four per module, twelve in total. Capture them
before access ends; without them this cannot be rebuilt like for like.

### Mechanics worth keeping

- Unlimited instances of each type, mixed freely at run time. Personality A with
  Audience B and Product C is a valid combination.
- One instance per type can be marked default and is pre-selected on every run.
- At least one module must stay active. The context is never empty.
- Fields carry a validation state: empty, awaiting review after auto-fill, or
  confirmed. Auto-filled content stays flagged until a human opens it.
- A "create or improve" action drafts a field from whatever is already filled in.

### How it maps onto this pipeline

The three modules correspond almost exactly to artefacts the growth-operating
gates already produce. That correspondence is why the tool is replaceable here.

| DNA module | Where it comes from in this pipeline |
|---|---|
| Personality | **The creator, not you.** Their voice, credentials and proof. You are the operator; the creator's brand is what the audience trusts. Drawn from their content and the deal terms. |
| Audience | The vetting memo. Specifically the verbatim audience comments and the closing line, "the one problem their audience keeps asking about". |
| Product | Gate 2's six lines: problem, promise, proof, delivery format, price, why now. |

One consequence worth stating plainly: a blank DNA field invites invention,
while the gates require evidence for every line. Filling Audience from a vetting
memo is strictly better than filling it from imagination, because the memo cites
real comments from real people.

### What replicates without the software

- **Reusable context.** This repository is the equivalent. The skill and its
  references load automatically in every session; vetting memos live in
  `growth-operating/vetting/`. Nothing is retyped.
- **Combination.** Naming a creator and an offer in a request achieves what
  selecting three tabs achieves.
- **Validation state.** The gates already do this more strictly. A field with no
  evidence is not "awaiting review", it fails.

The one mechanic with no equivalent here is the default pre-selection, which
saves clicks in a graphical tool and has no meaning in a conversation.

### Naming convention worth carrying over

Instances are named by combination, for example `CEO Profile | B2B Sales` or
`[Weight Loss] Women 40+`. The same convention suits memo filenames once more
than one creator is in play: creator, then niche, then offer.

---

## SalesFunnels.com — funnel mapping

**Stage served:** between 5 (offer design) and 7 (launch assets).

A drafting table, not a host. It maps sales pages, order bumps, upsells and
split-test variants onto a blueprint board, holds swipe files against them, and
the plan is then handed to whoever builds the pages. It does not publish pages
and it does not take payments.

| Takes | Returns |
|---|---|
| The funnel's intended structure: which pages exist, what each sells, where bumps and upsells sit | A blueprint board with swipe files attached, to hand to a builder |

### Where it belongs in the sequence

1. Gate 2 produces the offer: problem, promise, proof, format, price, why now.
2. **The map turns that single offer into a page-by-page structure.**
3. Ghostwriter OS writes the copy for each box on the map.
4. A page builder publishes them.
5. Whop takes the payment and splits it.

Step 2 is the one this tool owns. Skipping it is why launches end up as a single
page with no considered path through them.

### What replicates without it

A funnel map is a structure document: the pages in order, the job of each, and
the offer attached to each. That can be written here directly, and rendered as a
diagram when a picture helps. What does not replicate is the drag-and-drop
board, which is a comfort rather than a capability.

### The deal-terms gap this exposes

Order bumps and upsells are additional revenue on the same customer. **Your
50/50 split does not currently say whether it covers them.** A creator who
agreed to half of a 199 core offer may not expect to receive half of a 97 upsell
they did nothing to sell, or may assume they do. Both readings are reasonable,
which is exactly why it has to be written down before launch.

Add to the deal terms checklist: does the split apply to the core offer only, or
to every product sold through the funnel, including bumps, upsells and
downsells?

---

## Page builder and checkout

**Stage served:** 7 (launch assets).

Independent write-ups name Flozy Pro as the builder bundled with Monetise.
Unconfirmed against the platform itself.

### The rule that matters, whatever the builder is called

A page builder hosts pages and, in most cases, wants to host checkout too.
Checkout is the part that must not move.

Whop was chosen for one reason: its revenue split pays you and the creator
automatically from the same transaction, which removes the awkward conversation
about who owes whom. That split only fires on a Whop transaction.

**So: the funnel sells, Whop takes the money.**

| Page builder does | Whop does |
|---|---|
| Landing page, opt-in, video sales letter, upsell pages, thank-you page | Checkout, payment, membership access, delivery, revenue split |

Every buy button in the funnel points at the Whop checkout. If the builder's own
checkout is used instead, the split does not fire, the creator has to be paid by
hand, and payment resistance comes straight back.

**Check before committing to any builder:** can a button point at an external
checkout URL? A builder that forces its own checkout is unusable here, however
good its pages are.

### Consequence for deal terms

The deal terms checklist asks who owns the sales page copy. Add to it: who owns
the builder account, and what happens to the live pages if either side leaves. A
funnel hosted on the operator's account is leverage; one hosted on the creator's
is not. Decide it before launch, not after.
