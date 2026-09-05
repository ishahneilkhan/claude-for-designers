---
created: 2026-07-27
type: reference
status: complete
class: 4
tags: [ostad, batch-02, workbook, principles, design-taste]
project: EduBridge Bangladesh
---

# Design Taste — EduBridge Bangladesh

**What this file is for:** what "good" looks like on this project, in my own
words, tied to real content — not "clean and modern."

## My taste calls

1. **Trust signals are data, not icons.** A bare checkmark means nothing to a
   parent who's scared of being scammed. "Verified by EduBridge — NID and
   certificate checked" is taste. A checkmark with no label is decoration
   wearing a trust costume.

2. **Price is never demoted.** The total cost gets the same size and weight
   as the tutor's name — never smaller, never greyer. This is the number a
   worried parent scans for first, before they read anything else.

3. **One primary action per screen, named for the real outcome.** Not
   "Continue," not "Next." "Send Booking Request." "Proceed to Payment." The
   label should tell you what happens if you tap it, without needing to read
   anything else on the screen.

4. **Bengali is not the smaller font.** If English and Bengali strings sit on
   the same screen, Bengali gets the same size, weight, and prominence.
   Treating Bengali as a caption under the "real" English text is a taste
   failure specific to this market.

5. **A payment-adjacent screen stays calm.** Confirmation and receipt screens
   should feel quiet and uncluttered. Busy design on the screen where money
   moves reads as untrustworthy to a first-time mobile-money user — the
   opposite of what decoration is usually trying to do.

6. **Color follows meaning, not mood.** Navy is structure (headers, static
   info). Green is reserved for the one action that moves the booking
   forward. Green as a random accent on an unrelated icon dilutes what it
   means everywhere else on the screen.

7. **Loading and error states get the same care as the happy path.** A
   spinner with no message, on a connection that might drop from 4G to 3G
   mid-load, is not a minor omission — it's the exact moment a parent decides
   the app is broken and closes it.

These are the calls `design-taste.md` and `anti-ai-slop.md` together are
supposed to give Claude before it generates anything for this screen.
