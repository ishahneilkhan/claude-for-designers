created: 2026-07-27
type: reference
status: complete
class: 4
tags: [ostad, batch-02, workbook, principles, anti-ai-slop, student-editable]
project: EduBridge Bangladesh
---

# Anti-AI-Slop Rules

## YOUR TURN

**1. Find one output Claude gave you that you would not show a client. Name
the exact tell in one sentence.**

The booking screen Claude first generated had a centered hero with a soft
purple-to-blue gradient background behind the tutor's profile card — it looked
like a generic SaaS landing page, not a payment-adjacent trust screen a
worried parent needs to read fast.

**2. Add three slop patterns of your own.**

- **Verified badge as a decorative icon instead of a real element.** Claude
  drew a generic checkmark-in-a-circle with no label. Fix: badge must say
  "Verified by EduBridge" with a tap-to-expand showing what was checked —
  otherwise it's decoration, not trust.
- **Price shown only in an abbreviated form (e.g. "৳500/hr" in tiny grey
  text).** Fix: price must be full-size, same weight as the tutor name, never
  lower-contrast than surrounding text — this is the number parents scan for
  first.
- **A single global "Continue" button used for both "view details" and "confirm
  payment."** Fix: every screen gets exactly one primary action, and its label
  names the actual outcome ("Send Booking Request," not "Continue").

**3. List five words you ban in your product copy.**

- "Seamless" / "নিরবচ্ছিন্ন" — never true on 3G, don't promise it.
- "Empower" / "ক্ষমতায়ন" — nobody feels empowered booking a tutor, they feel
  relieved when it works.
- "Instant" — bKash/Nagad verification is not instant; saying so breaks trust
  the moment it's not.
- "Simply" / "শুধু" — as in "simply tap here." If it were simple I wouldn't
  need to say so.
- "Robust" —
