# EduBridge Design Tokens (draft — v1)

> Every color, space, and radius used in `my-booking-screen.html` traces to a
> token below. If a hex or px value appears in the HTML that isn't listed
> here, that's a bug to fix, not a style choice.

## Color

| Token | Value | Use |
|---|---|---|
| `--navy-900` | `#0A2540` | Brand primary — header bg, headings, CTA text on light |
| `--navy-700` | `#16375A` | Secondary navy — links, active states |
| `--green-600` | `#00A651` | Brand primary CTA, success accents |
| `--green-50` | `#E7F7EE` | Success/confirmation tint background |
| `--neutral-0` | `#FFFFFF` | Card surfaces |
| `--neutral-50` | `#F6F7F9` | Page background |
| `--neutral-200` | `#E1E5EA` | Borders, dividers |
| `--neutral-500` | `#6B7684` | Secondary/muted text |
| `--neutral-900` | `#171B21` | Primary text |
| `--amber-600` | `#B5710A` | Edge/warning accent (not alarming red) |
| `--red-600` | `#C0392B` | Error state only |

## Type

- Family: `'Noto Sans Bengali', 'Inter', system-ui, sans-serif`
  (Bengali-first pairing — Inter as Latin fallback for numerals/English labels)
- Scale: 12 / 14 / 16 / 20 / 24 (px) → `--text-xs` `--text-sm` `--text-base` `--text-lg` `--text-xl`
- Weight: 400 body, 600 emphasis/price, 700 headings only

## Space (4px base unit)

| Token | Value |
|---|---|
| `--space-xs` | 4px |
| `--space-sm` | 8px |
| `--space-md` | 16px |
| `--space-lg` | 24px |
| `--space-xl` | 32px |

## Radius

| Token | Value | Use |
|---|---|---|
| `--radius-sm` | 8px | inputs, small chips |
| `--radius-md` | 12px | cards |
| `--radius-lg` | 16px | sheets/modals |

## Touch

- `--touch-min`: 48px — minimum interactive target height (thumb zone, mid-range Android)

---
*Draft only — replace with your actual `tokens.md` from Class 5 if it
differs. This file exists so the screen has something concrete to trace to.*
