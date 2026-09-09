---
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

## The one rule your system has to enforce

**The One Confirm Color Rule.** Green appears only when it means trust
confirmed or action ready — the verified badge, the CTA, and the input focus
ring. Nothing else earns green. If a new element wants to stand out, it does
not get a new color; it earns green only by meaning the same thing the badge
already means.
