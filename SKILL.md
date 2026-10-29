---
name: idea-autopsy
description: "Stress-test a business idea — especially one an AI suggested — before anyone builds it. Use when the user says \"autopsy this\", \"is this a business or bullshit\", \"test this idea\", or pastes a startup/side-hustle idea and wants to know if it's real. Returns one of four verdicts: BUSINESS, BUSINESS WRONG OWNER (real idea, wrong constraints — says which), BULLETIN (it's really just content or information), or BULLSHIT, plus the smallest test that would prove it wrong. Built from a four-hour session in which an LLM pitched twelve businesses and eleven died."
---

# Idea Autopsy

## The idea in one line
LLMs are very good at generating plausible businesses and very bad at knowing which ones are real. The machine generates; a human decides. This skill is the deciding, written down. It is deliberately hostile: its job is to kill the idea. If the idea survives, build the smallest test, not the product.

## Hard rules
1. **Kill first, praise never.** Lead with what would make this fail. "Strong idea" is banned.
2. **Every claim needs a receipt.** A competitor must be named. A number must have a source. "Commonly" and "typically" are not evidence.
3. **Search before judging.** Run at least three web searches: incumbents, the graveyard (who tried this and died), and the pain (is anyone actually complaining).
4. **The owner's constraints are the law.** Hours per week, money available, audience size, location, and what they refuse to do. An idea that is a business for someone else can be bullshit for this person.
5. **End with a verdict and one test.** Never end with a list of considerations.

## Step 0 — Pin the constraints (ask if missing)
- Hours per week the owner actually has (and whether evenings-only).
- Revenue target and deadline (e.g. US$1,500/month in 6 months).
- Audience or distribution they already own (be honest: "a newsletter nobody reads" = none).
- Market they can reach (country, language, payment methods).
- What they refuse to do (cold calls, casework, marketing, physical presence).
- Unfair assets: data nobody else has, a licence, a captive customer base, a lived story, a skill that's rare.

## Step 1 — The Wrapper Test
Ask: **what does a general-purpose LLM not have that this idea needs?** There are only six answers that count. Mark which apply:
- **Private data** — records, registries, prices or history nobody can scrape or prompt for.
- **Action** — it does something in the world (sends, files, books, pays, delivers) rather than producing text.
- **Trust / licence** — a regulated role, a certification, a name people already believe.
- **Presence** — a body on the ground.
- **Captive audience** — people who already come to you.
- **Live specificity** — information that changes weekly and someone has to go and get.

If none apply, the idea is a wrapper. Verdict leans BULLSHIT. If the only thing it adds is "explaining" or "answering questions", verdict leans BULLETIN.

## Step 2 — The Crowd and the Graveyard
Search: `[idea] app 2026`, `[idea] alternative`, `[idea] shut down OR closed OR acquired`, `best [idea] tools`.
- Name at least five incumbents, with price and whether they're funded.
- Name anyone who tried this and died, and why.
- Rule of thumb for 2026: **any pain that makes the news already has ten apps within a quarter.** The question is not "is there a gap" but "why hasn't the gap been filled, and is that reason about to change?"
- **Look for the workaround.** Search `[problem] spreadsheet`, `[problem] "is there a tool"`, `[problem] "what's your system"`. People already duct-taping a spreadsheet and three apps together are demand with a receipt; people merely complaining are not. No workaround found usually means no one wants it badly enough to pay.
- If the incumbents are free (a government site, a bank's advice page, a safe-word card), the idea is competing with free. That is usually fatal.

## Step 3 — The Time Test
- Casework (clients, cases, calls, physical visits) does not fit evenings. Async products do.
- Count the hidden weekly chores: data updates, support, crawler breakage, chasing payments, partner admin. Add them to the build hours.
- If the owner becomes the bottleneck (approving every item, updating every rate), say so.

## Step 4 — The World-Condition Test
- Name the inflection the idea rides (a war, an oil price, a hiring slump, a platform backlash, a regulation).
- Ask: what happens to the idea if that condition reverses in six months? If the idea dies with the headline, it's a trade, not a business.
- Ask the reverse: what new condition would make it obsolete (the platform adds the feature, the government opens the data, the LLM gets the ability)?

## Step 5 — The Money Maths
Do the arithmetic with the owner's own target. Pick the model:
- **Subscription:** target ÷ price = customers needed; add 5–8% monthly churn for micro-business tools; state new customers needed per month just to stand still.
- **Per-case / service:** target ÷ price = cases per month; multiply by hours per case; compare to hours available.
- **Affiliate / lead-gen:** target ÷ payout per lead = leads; ÷ visitor-to-lead rate (assume 0.3–2%) = visits per month. State it under optimistic, realistic and pessimistic assumptions.
- **Marketplace:** state both sides' acquisition cost. Two-sided marketplaces are out of scope for a solo evenings builder unless one side is already captive.
If the maths needs the top of every range to reach the target, say the target is not reachable as specified.

## Step 6 — Fresh Eyes (when the idea is still alive)
If the idea has survived Steps 1–5, run a Goldfish pass: spawn at least three isolated reviewers with the Agent tool, each with one lens and no access to this conversation — Contrarian (why does this need to exist?), User Who Didn't Read the Manual (walk the first-time journey literally), Cost & Maintenance Realist (what it costs to run and who maintains it in a year). Pass them only the written idea and the constraints. Merge their findings by severity.

## Step 7 — Verdict
Exactly one of:
- **BUSINESS** — passes the wrapper test with at least one of the six, incumbents are beatable for a stated reason, fits the hours, survives the condition reversing, and the maths reaches the target without heroics.
- **BUSINESS, WRONG OWNER** — the idea is real (passes the wrapper test, incumbents beatable, demand with receipts) but it fails the owner's constraints: the hours, the presence it needs, the money or audience it needs first, or the thing the owner refuses to do. Say exactly which constraint fails. The fix is to change the constraints (a partner, a runner, more hours, a different target) or the owner — not to shrink the idea until it fits. Never downgrade a real idea to BULLSHIT because of the owner's calendar.
- **BULLETIN** — real demand, but what it really is is content, information or a stance. It may still be worth doing as an audience play — say so — but it is not a business on the stated clock.
- **BULLSHIT** — a wrapper, or free incumbents, or maths that doesn't close for anyone, not just this owner.

Then: **the smallest test** — one weekend, no build if possible — that would prove the verdict wrong. A landing page with a price, a spreadsheet sold once, ten cold emails, one post in the place the customer already is. State the kill line (the number by which date that means stop).

## Output format
```
VERDICT: BUSINESS / BUSINESS, WRONG OWNER / BULLETIN / BULLSHIT

Why (3 bullets max, worst first, each with a receipt)
What the LLM doesn't have here: [which of the six, or "none"]
Incumbents: [name, price, funded?] ×5 · Graveyard: [who died, why]
Time: [hours/week this really costs, and the hidden chores]
Condition it rides: [x] · If it reverses: [y]
Money: [the arithmetic, in one line, with the target]
Smallest test: [what, where, cost in hours] · Kill line: [number by date]
```

## Do not
- Suggest the idea "could work with more marketing". That is where bullshit hides.
- Replace the owner's target with a nicer one.
- Soften a BULLSHIT verdict because the owner is enthusiastic. Enthusiasm is the reason the skill exists.
- Pad. Three real findings beat fifteen considerations.
