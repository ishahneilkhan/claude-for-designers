---
created: 2026-07-27
type: reference
status: complete
class: 4
tags: [ostad, batch-02, workbook, principles, anti-ai-slop, student-editable]
---

# Anti-AI-Slop Rules

**What this file is for:** the list of things you refuse to ship, so you catch them before a client does.

**Why Claude needs it:** these patterns are Claude's defaults, because they are the most common patterns on the internet it learned from. Named in the folder, it avoids them. Unnamed, it produces them and waits for you to object.

**Which class:** Class 4, Claude as Critic. It runs alongside `design-taste.md` and the `/design-review` skill.

**`design-taste.md` says what good is. This file says what to refuse.** Together, filled in, they are the actual answer to "Sonnet produces bad design". The complaint is nearly always a folder with nothing in it about taste, not a model that cannot design. Same model, same prompt, these two files present: different output.

---

## EXAMPLE: the instructor's slop list (2026)

### Visual style slop

**Purple-to-pink gradients.** The default "AI app" aesthetic. If your screen has a gradient and you cannot defend the specific colors with a brand reason, change to a single brand color or remove.

**Generic "abstract tech" hero illustrations.** Floating geometric shapes, glowing orbs, low-poly heads, neural-network squiggles.

**Glassmorphism on everything.** Frosted-blur cards on every container.

**Identical card grid.** Five cards in a 5x3 grid, each with identical heights, identical button placements, identical type weights.

**Stock-photo-energy people.** Smiling diverse team in a meeting, hands typing on a laptop, lightbulb floating above a head.

**Random translucent dots and lines as decoration.**

### Layout slop

**Centered text where left-aligned would work.**

**Three-up feature grid as default.**

**Faux-3D buttons with multiple shadows.**

**Hero with title plus subtitle plus CTA plus secondary CTA plus signup form plus social proof plus arrow pointing down.**

### Copy slop

**"Empower." "Seamlessly." "Leverage." "Robust." "Intuitive." "Delight."**

**Three-item lists where two would do.**

### Component slop

**Toast notifications for everything. Modals for things that should be a page. Empty states that say "No data yet" with a sad cloud. Loading spinners that show indefinitely. Generic error messages.**

### The meta-rule

The strongest anti-slop signal is **specificity**. When Claude proposes something generic, ask: "What would change about this design if we knew the user is a 45-year-old auntie in Comilla checking her son's tutor at 9pm on a borrowed phone?" If nothing changes, the design is not specific enough.

---

## YOUR TURN

**1. Find one output Claude gave you that you would not show a client. Name the exact tell in one sentence.**

The first booking screen Claude generated had a centered hero with a
purple-to-blue gradient behind the tutor's profile card — it looked like a
generic SaaS landing page, not a payment-adjacent trust screen a worried
parent needs to scan fast.

**2. Add three slop patterns of your own.**

- **Verified badge as a decorative icon instead of a real element.** Claude
  drew a checkmark-in-a-circle with no label. Fix: badge must say "Verified
  by EduBridge" with a tap-to-expand showing what was checked — otherwise
  it's decoration, not trust.
- **Price shown only in abbreviated, low-contrast text (e.g. "৳500/hr" in
  tiny grey type).** Fix: price must be full-size, same weight as the tutor
  name, never lower-contrast than surrounding text — this is the number
  parents scan for first.
- **A single global "Continue" button used for both "view details" and
  "confirm payment."** Fix: every screen gets exactly one primary action, and
  its label names the actual outcome ("Send Booking Request," not
  "Continue").

**3. List five words you ban in your product copy.**

- "Seamless" / "নিরবচ্ছিন্ন" — never true on 3G, don't promise it.
- "Empower" / "ক্ষমতায়ন" — nobody feels empowered booking a tutor, they feel
  relieved when it works.
- "Instant" — bKash/Nagad verification is not instant; saying so breaks trust
  the moment it isn't.
- "Simply" / "শুধু" — as in "simply tap here." If it were simple I wouldn't
  need to say so.
- "Robust" — empty word on a parent-facing screen. Say what's actually true:
  "checked before every booking," not "robust verification."

**4. Write your own version of the specificity test.**

A 42-year-old mother in Dhaka, on a three-year-old Android phone, checking
this screen at 9pm after her son mentions the exam is in six weeks — if the
badge, the price, or the CTA label don't change when I picture her instead of
"a user," the design isn't specific enough yet.

**5. Which rule on this list do you break on purpose, and what is your defense?**

I break "three-item lists where two would do" on the price breakdown card —
session fee, platform fee, total is three rows, not two. My defense: this
isn't a marketing list of adjectives, it's a literal fee breakdown, and the
contract treats hidden or late-revealed fees as a hard blocker. Cutting a row
there would be hiding a cost, not tightening copy — the rule protects against
padding, and nothing here is padding.
