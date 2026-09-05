---
created: 2026-07-27
type: note
status: complete
tags: [edubridge, class-4, critique]
project: EduBridge Bangladesh
---

# EduBridge BD: Critique Notes

### Screen being critiqued

Tutor booking request screen, v0.1, generated straight from the confused v1
client brief (desktop-first, English-only, card-checkout, student-as-primary
assumptions baked in).

Layout: a centered hero section with the tutor's large profile photo
full-bleed at the top. Below it: tutor name in bold, a generic "Verified"
badge (checkmark icon, no label explaining what was checked), star rating,
hourly rate shown in small grey text ("৳500/hr"), a short bio paragraph, and
one purple-gradient "Book Now" button centered at the bottom. No session
total shown, no payment method mentioned yet — that's assumed to be a card
form on the next screen.

### Perspective 1: confused user on a 3G phone

On a 5.5" screen, the full-bleed hero photo pushes everything else below the
fold — the price, the badge, and the CTA all require a scroll on first
paint. On a throttled 3G connection, the hero photo is also the heaviest
asset on the screen, so the user is staring at a blank grey box for the
first two to three seconds with nothing else rendered yet. Finding: the
single most important information (price, verification) is the least
visible information on the slowest connections.

### Perspective 2: skeptical parent afraid of being scammed

The "Verified" badge is a bare checkmark with no label — it doesn't say what
was verified, by whom, or when. A parent who is specifically afraid of an
unqualified tutor gets a decoration that looks like reassurance but carries
no actual claim. Finding: the badge fails the one job the brief says trust
signals have to do — it would look identical whether or not any document was
ever checked.

### Perspective 3: Bengali-first reader unfamiliar with financial English

Every string on the screen is in English, including "Book Now," the star
rating label, and the bio. For a parent whose stronger language is Bengali,
the button that starts a money transaction is the one piece of text they're
least equipped to read with full confidence. Finding: the highest-stakes
action on the screen (committing to pay) carries zero localization, while
low-stakes decorative text (the bio) gets the same English-only treatment —
priority is inverted.

### /design-review findings

- Price (৳500/hr) is set in small, low-contrast grey text — directly
  violates `design-taste.md` rule 2 (price is never demoted).
- The badge is a plain checkmark icon with no label — violates
  `anti-ai-slop.md` YOUR TURN #2 (badge as decoration instead of a real
  element).
- The CTA uses a purple gradient with no relationship to the navy/green brand
  tokens — textbook `anti-ai-slop.md` visual-style slop, no brand reason
  given for the specific colors.
- No fee breakdown or total is shown anywhere on this screen — the actual
  amount only appears after tapping through, which the project contract
  names as a hard blocker (`claude-contract.md`: "no fee changes late in a
  flow").

### /heuristic-evaluation findings (Nielsen pass)

- **Visibility of system status:** fails. Nothing on screen tells the parent
  what stage of the booking flow they're in, or what happens after "Book
  Now" is tapped (payment screen? confirmation? another form?).
- **Match between system and the real world:** fails. "Book Now" implies an
  instant action; tapping it actually opens a multi-step payment flow. The
  label doesn't match what happens.
- **Error prevention:** fails. With no price shown upfront, there's no
  moment for the parent to notice a mistake (wrong tutor, wrong price
  expectation) before committing to the next screen.
- **Aesthetic and minimalist design:** fails, but for the opposite of the
  usual reason — the screen isn't cluttered, it's under-informative. A
  minimalist screen that omits the price isn't restraint, it's a missing
  requirement.

### /persona-acid-test findings

Running the same three lenses (3G user, skeptical parent, Bengali-first
reader) through the automated pass surfaced the same three findings as the
manual run above, plus one the manual pass missed: the star rating has no
count next to it ("4.8 ★" with no "(12 reviews)"), which reads as fabricated
or unverifiable to a skeptical-parent lens specifically — the automated pass
caught this because it re-ran the skeptical-parent question against every
individual element on the screen rather than just the ones I'd already
flagged by eye.

### Decision

**Direction that wins:** price and verification move to the top of the
screen, above the fold, before the tutor photo. The badge becomes "Verified
by EduBridge" with a tap-to-expand showing what was checked. The CTA becomes
"Send Booking Request" in the brand green, not a purple gradient. The full
session total (not just hourly rate) is shown on this screen, not deferred
to the next one.

**Finding that decided it:** the Perspective 1 finding (3G load order) and
the contract's hard-blocker rule on late fee reveals both point the same
direction — whatever the parent needs to trust the booking has to render
first and cannot wait for a heavier asset (the hero photo) to finish
loading. The photo lost priority; the price and badge won it.

**What the other direction lost on:** keeping the large hero photo at the
top would have looked more "premium" in a static screenshot, but it fails
the actual constraint this project is designed against — a mid-range Android
phone on inconsistent connectivity, where the heaviest element on the screen
should never be the one blocking the most important information.
