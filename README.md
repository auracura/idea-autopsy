# Idea Autopsy

A Claude skill that tells you whether a business idea — especially one an AI suggested — is a **BUSINESS**, a **BUSINESS, WRONG OWNER**, a **BULLETIN** (really just content), or **BULLSHIT**. It is deliberately hostile. Its job is to kill the idea; if the idea survives, it hands you the smallest test that would prove it wrong, with a kill line.

## Where it came from

I spent four hours letting an AI pitch me side businesses: invoice-chasing tools, Caribbean land registries, verified-handmade badges, graduate-to-trades content sites, an "Etsy without AI slop". Eleven of twelve died — to a free government website, to a chatbot that already answers the question, to a funded team already running the race, and to my own calendar.

The machine generated. I decided. The deciding was a repeatable set of tests, so I wrote them down. This is them.

## The tests, in order
1. **The Wrapper Test** — what does a general-purpose LLM *not* have that this idea needs? Private data, action, trust/licence, presence, a captive audience, or live specificity. None of the six = wrapper.
2. **The Crowd and the Graveyard** — name five incumbents with prices; name who tried this and died. In 2026 any pain that makes the news has ten apps within a quarter.
3. **The Time Test** — casework doesn't fit evenings. Count the hidden weekly chores.
4. **The World-Condition Test** — what does the idea ride, and what happens when it reverses?
5. **The Money Maths** — with the owner's own target, not a nicer one.
6. **Fresh Eyes** — isolated reviewers, one lens each, for anything still alive.
7. **Verdict + smallest test + kill line.**

## What it did in testing (examples/)
- `01-ai-meal-planner.md` — textbook LLM slop. BULLSHIT. Found the graveyard on its own: Yummly (Whirlpool) shut 2024, Mealime (Albertsons) shutting Oct 2026.
- `02-tax-prep-service.md` — a real service I'm building, disguised. First verdict: BULLSHIT on the stated hours. It found that the "paperless" filing route requires a signed form physically dropped at a government office during business hours, and that the government is closing the wedge. I didn't know that.
- `03-one-page-site-builder.md` — Carrd, described as if proposed today. BULLSHIT, because Carrd exists. Fair — and a limit: the skill judges an idea *today*; it cannot tell you what would have worked in 2016.
- `04-handmade-marketplace.md` — Goimagine, disguised. BULLSHIT. It identified the real company, its US$400k raise, its US$40k/month burn, and its closure on 23 March 2026.
- `05-tax-prep-constraints-fixed.md` — the same tax service with a paid runner and more hours. Verdict moved to **BUSINESS, WRONG OWNER**: wrapper test passed, hours now fit, but the owned audience is 7× too small for the target. That is the behaviour you want — the verdict moves with the constraints, and it names which one still fails.
- `06-decyde-my-own-product.md` — **Decyde, my own live product.** BULLETIN. It found that I was competing with a free HubSpot tool, that a near-identical product (Lorelight) had shut down because its reports changed nobody's behaviour, and that my go-to-market ate my entire weekly time budget. I've withheld the test and kill line it gave me because I'm running them.

## I ran it on my own builds
Two of the examples above are mine: a tax-filing service (kept unnamed — it has customers) and Decyde (named — it's already public). Neither came out BUSINESS. One moved to BUSINESS, WRONG OWNER when I fixed the constraints it flagged; the other is a BULLETIN. I also ran it on two older ideas of mine that aren't in this repo. Both died. I'd rather know now than in month nine.

Six runs, zero BUSINESS. Every kill came with a receipt I could check. Make of that what you will about AI-generated business ideas — and about mine.

## Install
Copy `SKILL.md` into your Claude skills folder (`.claude/skills/idea-autopsy/SKILL.md`) and say "autopsy this".

## Limits
- It judges ideas *today*; it does not time-travel.
- It is only as good as its searches. Check the receipts.
- It is tuned to kill. If you want encouragement, this is the wrong tool.
