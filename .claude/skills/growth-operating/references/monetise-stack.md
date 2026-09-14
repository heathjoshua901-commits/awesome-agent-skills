# Monetise stack: what each tool takes and returns

Operational notes on the tools inside Monetise, kept so their useful behaviour
can be reproduced without the software. Recorded because access ends if the
refund completes.

For each tool: what you feed it, what it returns, and which pipeline stage it
serves. Stage numbers refer to the table in `SKILL.md`.

---

## Ghostwriter OS

**Stages served:** 3 (outreach) and 7 (launch assets).

**A third-party product, not built by Monetise.** It runs at
`dashboard.ghostwriteros.ai` with its own version numbers per agent and its own
release cadence. Interface strings appear in Portuguese behind the English
labels, so it is likely a Brazilian or Latin American SaaS that Monetise
bundles. Two consequences: it is probably purchasable on its own, and whether a
Monetise refund ends access to it is a separate question that has to be asked
directly.

### Navigation

| Section | What it holds |
|---|---|
| DNAs | Campaign DNA context modules |
| Projects | Marked beta |
| Agents | Single-purpose generators, individually versioned |
| Flows | Multi-step chains of agents |
| Images | Image generation |
| Archive | Past output |
| Instructions | Product documentation |

### Campaign DNA

Reusable context fed to the agents, so the same brand, audience and offer facts
are not retyped per run. A context-management layer, not a generator.

#### Structure

Three independent module types. Each holds four fields.

| Module | Question it answers |
|---|---|
| Personality | Who is speaking: brand, tone of voice, credentials |
| Audience | Who is being spoken to: ideal customer, beliefs, pain points |
| Product | What is being offered: offer, problem solved, solution |

#### Personality fields

Recorded from the live editor. The other two modules hold four fields each and
are still uncaptured.

| Field | What it asks for |
|---|---|
| Author Biography | Yourself and the company, with at least three main achievements: client numbers, accomplishments, awards, appearances |
| Author/Brand Voice | How the brand sounds |
| Credentials, Proof and Evidences | The proof behind the claims |
| Banned Words and Phrases | Words the output must never use |

#### The validation marker measures attention, not accuracy

Opening a flagged tab turns its marker from amber to blue. No edit is required
and none is checked. Observed directly: the Author Biography marker read blue on
one screen and amber on another with the body text byte-identical between them.

So a fully blue DNA means every tab has been looked at. It does not mean a
single claim in it is true. Treat the marker as a reading log.

#### Author/Brand Voice

The field takes either a description of the style and tone, or pasted examples
of real texts, emails and posts that carry the voice. **Pasted examples are the
better input**, and for a creator they are the only honest one, because their
voice is evidenced in what they have already published.

An agent named "Voice of the Author/Brand" turns those examples into a
structured document. The structure is worth reproducing:

1. **Fundamental Vocal Identity** — voice essence in adjectives, brand persona,
   relationship with the audience
2. **Personality Pillars** — two or three named traits, each with a sentence on
   how it shows up in the writing
3. **Base Linguistic Profile** — signature expressions and recurring phrasing

That is a usable template for capturing any creator's voice. Collect twenty of
their posts, produce the document, and keep it beside their vetting memo.

Two of the four fields are worth carrying over regardless of the software.

**Credentials, Proof and Evidences** is Gate 2's proof line under another name.
A creator with nothing to put in this field has no offer, and the gate already
says so.

**Banned Words and Phrases** has no equivalent in the gates and should. Every
creator has words that do not sound like them, and a list of those is faster to
apply than a description of their voice. Collect it during the first call.

#### The trap this module sets

The Personality module asks for "your business or brand identity", so the
obvious move is to fill it with your own. For a growth operating campaign that
is the wrong answer. The audience is buying from the creator, and the copy is
published under their name. Personality belongs to them.

Keep a separate Personality for your own consultancy if you market it. Never let
that one be the default when writing campaign copy for a creator.

#### Audience fields

Recorded from the live editor.

| Field | What it asks for |
|---|---|
| Ideal Client Profile | The ideal client in detail: characteristics, pain points, desires |
| The Persuasive Premise | The one belief that turns a prospect into a customer |
| Testimonials | Customer testimonials |
| Keywords | Terms the audience uses or searches |

The Ideal Client Profile field states outright that it "fuels almost all
agents". It is the highest-leverage field in the entire system, which makes it
the most damaging one to invent.

#### The generation loop

Both Ideal Client Profile and The Persuasive Premise are field names **and**
agent names. The workflow the tips describe is: run the agent, paste its output
into the matching DNA field, and that field then becomes context for every
other agent.

Nothing external enters this loop. A generated persona becomes the evidence base
for generated copy, which reads as confirmation that the persona was right.

**The rule:** at least one field in Audience must contain something a real
person actually said or did. Verbatim comments from the vetting memo, a
transcript line from a discovery call, a support ticket. Without that, the loop
is closed and the whole campaign is arguing with itself.

#### Testimonials is not a writing field

Every other field can hold a working hypothesis. This one cannot. A testimonial
is a claim that a named customer said a specific thing. Auto-filled content here
is a fabricated endorsement, and publishing it is a misrepresentation regardless
of how the text got there.

Fill it only by pasting words a real customer actually wrote, or leave it empty.
If the create-or-improve action has ever been used on this field, clear it.

#### Product/Service fields

Recorded from the live editor. All twelve fields are now captured.

| Field | What it asks for |
|---|---|
| The Problem | The main problem the audience faces, one pain at a time |
| The Solution | How the product resolves it |
| The Offer | What is actually being sold |
| Keywords | Terms attached to the product |

The Problem field frames the pain as an "Enemy" and calls it the foundation of
all communication. That matches Gate 2's first line in intent. It differs in
sourcing: the field does not say where the problem should come from, while the
gate requires it in the audience's own words, taken from real comments, and
explicitly not from the creator's framing.

A proprietary framework named D.O.R.E.S. is offered for qualifying a problem
statement, along with an agent called Unique Problem Mechanism that does not
appear in the favourites view. Its definitions are course material and are
deliberately not reproduced here. The structural point is enough: the tool
expects a problem statement to be tested against fixed criteria before it is
trusted, which is the same instinct the gates encode.

#### The complete map against Gate 2

| Gate 2 line | DNA field |
|---|---|
| Problem | Product → The Problem |
| Promise | Product → The Solution |
| Proof | Personality → Credentials, and Audience → Testimonials |
| Delivery format | Product → The Offer |
| Price | Product → The Offer |
| **Why now** | **nothing** |

Eleven distinct fields across three modules, and not one of them asks why the
buyer should act this month rather than bookmark the page. Urgency is the line
that most often decides whether an offer converts, and the system has no slot
for it at all.

Keep Gate 2's sixth line. When feeding this tool, carry "why now" into The Offer
by hand, because nothing in the interface will prompt for it.

#### Mechanics worth keeping

- Unlimited instances of each type, mixed freely at run time. Personality A with
  Audience B and Product C is a valid combination.
- One instance per type can be marked default and is pre-selected on every run.
- At least one module must stay active. The context is never empty.
- Fields carry a validation state: empty, awaiting review after auto-fill, or
  confirmed. Auto-filled content stays flagged until a human opens it.
- A "create or improve" action drafts a field from whatever is already filled in.

#### How it maps onto this pipeline

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

#### What replicates without the software

- **Reusable context.** This repository is the equivalent. The skill and its
  references load automatically in every session; vetting memos live in
  `growth-operating/vetting/`. Nothing is retyped.
- **Combination.** Naming a creator and an offer in a request achieves what
  selecting three tabs achieves.
- **Validation state.** The gates already do this more strictly. A field with no
  evidence is not "awaiting review", it fails.

The one mechanic with no equivalent here is the default pre-selection, which
saves clicks in a graphical tool and has no meaning in a conversation.

#### Naming convention worth carrying over

Instances are named by combination, for example `CEO Profile | B2B Sales` or
`[Weight Loss] Women 40+`. The same convention suits memo filenames once more
than one creator is in play: creator, then niche, then offer.

### Agents

Single-purpose generators, each independently versioned and updated. Observed in
the favourites view, grouped here by the pipeline stage they would serve.

**Offer design, Gate 2 territory**

| Agent | Stated purpose |
|---|---|
| Ideal Customer Profile | Understand the ideal client better than they understand themselves |
| High-Value Customer Compass | Find ideal clients who pay more |
| The Persuasive Premise | Define the one belief that turns prospects into customers |
| Problem & Promise | Define the problem and promise the product solves |
| Unique Selling Proposition | Make the difference clear |
| Offer Generator | Create an offer people feel stupid saying no to |
| High-Ticket Product Generator | Turn a high-ticket idea into a delivery plan |

**Launch assets, stage 7**

| Agent | Stated purpose |
|---|---|
| Ad Funnel | Full funnel from first contact to conversion |
| Ads Generator | Content into ads, chosen by funnel stage |
| Content to Ads | Any content into ads |
| Email Subject Lines | Subject lines for open rate |
| Carousel Generator | Content into carousels |
| Instagram Story | Story sequences to sell or build authority |
| Presentation Generator | Ideas into slides |
| Lead Magnets Generator | Ideas into lead magnets |

**Voice**

| Agent | Stated purpose |
|---|---|
| Writing Analyzer | Recreate the author's authentic style with precision |
| Universal Adapter | Adapt any text to match the business DNA |

Writing Analyzer is the most relevant agent in the list for this business model,
and not for the obvious reason. Personality DNA has to hold the creator's voice,
not the operator's. Feeding a creator's existing posts through a style analyser
is the mechanical way to get it there. The equivalent here is pasting a sample
of their writing and asking for the voice to be matched.

### Flows

Multi-step chains that run several agents in sequence: Short Content, Instagram
Positioning, Ads, VSL Funnel, Campaign DNA, Direct Sale Campaign, Instagram
Editorial Strategy, Newsletters, YouTube from Idea to Click, Instagram Content,
High Ticket Funnel, and **Growth Operator: Webinar Flow**.

The last one is named for this exact business model and describes a path from a
business audit through to a complete webinar funnel and waitlist. It is the
single asset in the whole stack built for what you are doing, and it is worth
opening and reading before any decision that ends access.

### The inversion to watch

Every agent above generates from the Campaign DNA you typed. Nothing in the
chain checks whether the DNA was true. An Offer Generator fed an invented
audience returns a confident, well-written offer for a person who does not
exist.

The gates in `SKILL.md` run the other way. Evidence first, offer second. Use the
agents to phrase an offer the gates have already justified, never to discover
one.

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
