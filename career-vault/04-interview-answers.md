---
created: 2026-09-09
type: workbook
status: complete
tags: [ostad, batch-02, career-vault, class-08, interview]
---

# Interview Answer Bank

## YOUR TURN

### 1. What do you say when someone insinuates AI did your work?

**Decision one:** I caught that the brief's own success metric (tutor
signups) didn't measure the person actually making the booking decision
(the parent), and rewrote the brief around the parent as primary user.

**Decision two:** I rejected the client's assumed card-first payment flow
and argued for bKash/Nagad as primary, backed by a screen count — 3 to 4
extra screens and new error states their UK conversion data never had to
account for.

**Decision three:** I moved the price and verification badge above the
tutor photo after a 3G-load-order critique showed the heaviest asset (the
photo) was blocking the most important information on the slowest
connections.

**Your answer:**

"Fair question. The way I work is that I direct the decisions and Claude
makes the execution fast. On this project specifically: I caught that the
brief was measuring the wrong person's behavior and rewrote it around the
parent, not the tutor. I rejected the card-first payment flow the client
assumed and made the case for bKash/Nagad with a screen count, not just an
opinion. And I moved the price above the fold after tracing what actually
loads first on a throttled 3G connection. The HTML is the easy part. What
you're hiring is the judgment that the brief was wrong."

### 2. STAR: a time you disagreed with someone who outranked you

**Situation:** The EduBridge brief measured success by tutor signups, but
my read of the brief's own context showed parents were the ones who decide
and pay. The client's team (Jamie, the PM) had not flagged this as a
problem.

**Task:** I had to decide whether to design against the metric as written
or push back on it before starting, knowing pushback on a paying client's
own success metric risked reading as overstepping.

**Action:** I wrote it up as a reported gap, not an opinion — named which
of the six brief-completeness points was failing, cited the specific
contradiction (metric measures tutor signups, parent makes the booking),
and sent one direct question asking which side to design for, with a date.

**Result:** The gap was acknowledged rather than dismissed, and I proceeded
designing for the parent, which the brief's own trust and payment concerns
already pointed to anyway.

**What I learned:** Framing a disagreement as a reported gap instead of a
concern is what keeps it answerable instead of dismissible. "Section 3 has
no success metric that matches the primary user" gets you an answer.
"I have concerns about the metric" gets you told to just proceed.

### 3. STAR: a time you were wrong

**Situation:** My first version of the booking screen led with a large
tutor photo at the top, centered, with the price and verification badge
below the fold — I assumed a photo-forward layout would read as more
trustworthy and premium.

**Task:** I needed to design the highest-trust screen in the flow, the one
right before payment, for a parent who is specifically worried about being
scammed.

**Action:** I ran the screen through three perspectives by hand — a
confused user on 3G, a skeptical parent, a Bengali-first reader — before
running the automated critique pass.

**Result:** The 3G-user lens showed the heaviest asset on the screen (the
photo) was blocking the price and badge from rendering first, on exactly
the connection this project is designed against. I rebuilt the layout with
price and verification above the photo.

**What I learned:** "Premium-looking" and "trustworthy on a slow
connection" are not the same design problem, and I'd defaulted to the
first one without checking against the actual device constraint. Now I
check the load order against the target device before I check how a
layout looks in a static screenshot.

### 4. STAR: the project you are proud of

**Situation:** EduBridge's brief arrived contradictory across three
versions — desktop-first vs mobile-first, card-only vs bKash-first,
student-primary vs parent-primary — and I was the one holding it before any
design work started.

**Task:** Resolve the contradictions with evidence rather than guesswork,
then design and build one real screen — the parent-facing booking summary —
end to end.

**Action:** I ran a six-point completeness test on the brief, wrote three
answers with honest confidence labels instead of guessing, sent a scope
email naming the specific gaps and one question each, then built the
screen with a token system locked in first so color and spacing decisions
didn't get relitigated during the build.

**Result:** A working HTML screen, mobile-first, tokens traced end to end,
with the price and trust badge above the fold and bKash/Nagad as the
primary payment path — plus three extra states (loading, error, and a
long-name edge case) nobody had asked for.

**What I learned:** The screen only works because the brief work happened
first. Every fix I made in the build — payment order, information
hierarchy, fee transparency — traces back to a specific gap I found before
I opened Figma.

### 5. Answer the five process questions

**How do you work on a brief?**

I assume the brief is out of date before I open it, because on this
project it was — three versions contradicted each other on device,
payment, and who the primary user even was. I read every version together
rather than one at a time, because the contradictions only show up side by
side. Then I run a six-point completeness test and answer only the
questions nobody else can answer for me, each with a confidence label. On
EduBridge, three of my answers were genuinely uncertain and I marked them
that way instead of guessing confidently — one of them (Bengali as
required vs optional) turned out to still be unresolved between two people
on the client side, which is exactly the kind of thing a confident guess
would have hidden. *Source: `brief-v3-interrogated.md`.*

**Your boss changes the brief halfway through. What do you do?**

I check whether it's a revision or new scope, because they get handled
differently — a revision I absorb, new scope gets a written estimate before
I start on it. On EduBridge, video calling and a tutor verification badge
both surfaced in the client's PM thread after the 3-lakh budget was
already agreed. I didn't build either of them into the current cycle;
I named them explicitly as out-of-scope in the engagement doc, so
they're documented as new work rather than absorbed silently.
*Source: `engagement.md`.*

**How do you negotiate?**

I try to get scope written down before a number exists, because once a
number exists everything becomes a negotiation instead of a definition. On
EduBridge, the client's team was treating the payment integration as a
"logo swap" from card to bKash. I didn't argue with that framing directly —
I counted the actual screens the bKash/Nagad flow adds (app-switch, PIN,
OTP, hand-typed transaction ID, async verification wait) against their own
UK conversion data, which gave the client a number to react to instead of
my opinion to argue with. *Source: `engagement.md`, `critique-notes.md`.*

**How do you plan a piece of work?**

I break the brief into what's in scope and what's explicitly out before
I design anything, then I build one screen completely rather than
sketching the whole product thinly. On EduBridge that meant naming four
things as explicitly out of scope (video calling, search, tutor onboarding,
profile translation) before touching Figma, then shipping one screen — the
booking summary — with its loading, error, and edge-case states, not just
the happy path. *Source: `engagement.md`, Class 6.*

**How do you pitch an idea?**

I bring the alternative with the pitch, not just the idea on its own.
When I moved the price and verification badge above the tutor photo, I
didn't just present the new layout — I showed the old layout, the specific
finding that decided it (the 3G load-order problem), and what the new
layout gives up (a less "premium-looking" first screenshot). Naming what
you lose is what makes the pitch credible instead of one-sided.
*Source: `critique-notes.md`.*

### 6. What three questions do you ask them?

1. "What's a design decision the team made recently that someone
   internally disagreed with — how did that get resolved?"
2. "What does the path from junior to mid-level actually look like here —
   not the title change, but what scope of work shifts?"
3. "How does the team use AI in the design process today, and is there
   anything you've deliberately decided not to use it for?"
