created: 2026-07-27
type: reference
status: complete
tags: [edubridge, class-5, workbook, design-tokens]
project: EduBridge Bangladesh
---

# EduBridge BD: Design Tokens

**What this file is for:** the named values your design is made of, written once so you stop retyping hex codes into every prompt and every Figma layer.

**Why Claude needs it:** without it, "use a nice green" produces a different green every session. With it, Claude writes `#00A651` because you told it what `accent.primary` means, and your Figma variables and your built screen finally agree.

**Which class:** Class 5. Class 6 pastes this file into the prompt that builds the screen.

## Color

| Token | Value | Use for |
|---|---|---|
| `bg.surface` | `#FFFFFF` | Card backgrounds, content areas |
| `bg.inverse` | `#0A2540` | Header bar, top price/trust summary block |
| `text.primary` | `#171B21` | Tutor name, body copy, primary content |
| `text.secondary` | `#6B7684` | Detail labels ("তারিখ ও সময়", "শিক্ষার্থী") |
| `text.muted` | `#9CA3AF` | Placeholder text, disabled states |
| `accent.primary` | `#00A651` | Primary CTA, verified badge, input focus — and nothing else |
| `accent.danger` | `#C0392B` | Error states (slot taken, payment failed) |
| `border.default` | `#E1E5EA` | Card borders, row dividers |

## Type

Font: `'Noto Sans Bengali', 'Inter', system-ui, sans-serif` — system stack, no webfont load, renders instantly on 3G.

| Token | Size | Weight | Line height | Use for |
|---|---|---|---|---|
| `text.display` | 20px | 700 | 1.3 | Total session price — the number being decided on |
| `text.heading` | 18px | 700 | 1.3 | Tutor name |
| `text.body` | 15px | 400 | 1.5 | Detail rows, bio text |
| `text.body.small` | 13px | 400 | 1.4 | Secondary labels, review counts |
| `text.label` | 12px | 600 | 1.2, 0.05em tracking | Section labels, badge text |

## Spacing and radius

Base unit: 4px.

| Token | Value |
|---|---|
| `space.1` | 4px |
| `space.2` | 8px |
| `space.3` | 12px |
| `space.4` | 16px |
| `space.6` | 24px |
| `space.8` | 32px |
| `radius.sm` | 8px |
| `radius.md` | 12px |
| `radius.full` | 100px |

## Motion

| Token | Duration | Easing | Use for |
|---|---|---|---|
| `motion.fast` | 80ms | ease-out | CTA press feedback |
| `motion.default` | 160ms | ease-in-out | Card expand, tab switch |
| `motion.slow` | 220ms | ease-in-out | Screen transition |

Ceiling is 220ms because the target device is a mid-range Android on 4G that
can drop to 3G — a longer transition reads as a hang, not as polish.

## The receiver's test — three questions answered

**1. "What happens when…?" — empty, error, loading, the forty-character name.**

Empty state uses `text.muted` (`#9CA3AF`) at `text.body` size, never a blank
box. Error state uses `accent.danger` (`#C0392B`) for the message text and
`bg.surface` with a `border.default` border for the card — never a full red
background, which reads as more alarming than the situation (a taken slot,
not a failed payment). Loading state shows a spinner using `accent.primary`
against `bg.surface`, with a one-line message in `text.body.small` — never
a bare spinner with no text. A forty-character tutor or student name wraps
using `word-break: break-word` inside its card; it never truncates with an
ellipsis, because a parent needs to confirm the full name before paying.

**2. "Which of these is the real value?" — two greens, three spacings.**

There is exactly one green in this system: `accent.primary` (`#00A651`).
Any other green seen in a mockup or reference is not a token — it does not
exist in this file, so it does not ship. On spacing: `space.4` (16px) is
the real value for card padding and CTA padding; `space.3` (12px) is for
tight internal gaps (icon-to-label); `space.6` (24px) is for separation
between stacked cards. If a screen shows a fourth spacing value that isn't
in the Spacing table above, it is a mistake, not a new token — round it to
the nearest listed value instead of inventing one.

**3. "Do I build this once or five times?" — component, or coincidence.**

The CTA button is one component (`button/primary`, with `Default` and
`Pressed` variants) — build it once, reuse everywhere a primary action
appears. The price-breakdown row (label left, value right, `border.default`
divider) is a component too — it repeats identically across session fee,
platform fee, and total, so it is not a coincidence that they look alike.
The tutor avatar-and-name row is also one component, reused on the booking
summary, the tutor profile, and anywhere else a tutor is referenced. Only
the top navy summary block (`bg.inverse`) is screen-specific and does not
need to be a component — it appears once, on this screen only.

## The one rule your system has to enforce

**The One Confirm Color Rule.** Green appears only when it means trust
confirmed or action ready — the verified badge, the CTA, and the input focus
ring. Nothing else earns green. If a new element wants to stand out, it does
not get a new color; it earns green only by meaning the same thing the badge
already means.
