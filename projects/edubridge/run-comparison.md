# Run Comparison: Payment Confirmation Screen

**Prompt used:** "Design a payment confirmation screen for EduBridge."

## Output 1 — No context

A payment confirmation screen would typically include:
- Success icon (green checkmark) at the top, large
- "Payment Successful" heading, clean sans-serif font
- Transaction summary card: amount paid, date, transaction ID, payment
  method (Visa/Mastercard icon)
- "Download Receipt" and "Continue to Course" buttons
- Light animation (checkmark bounce/fade-in)
- Assumes fast internet, so a lottie animation or video confirmation
  could work
- Layout responsive, but primarily assumes desktop/wide-screen browsing

## Output 2 — With EduBridge context.md

- Payment method logo: bKash/Nagad icons shown (not Visa/Mastercard) —
  the trusted, familiar method here
- Screenshot-friendly design: full transaction info visible on one
  screen without scrolling, since parents screenshot confirmations
- No hidden fee or late charge shown on this screen — only the quoted
  amount, to protect trust
- Lightweight design: no animation or lottie, since 3G connections can
  drop it — just a simple static checkmark
- Bangla + English together, amount in large numerals, date in local
  format (DD/MM/YYYY)
- Mobile-first, one-hand usable — built for shared family phone use in
  the evening

## What changed (4-6 bullets)

- Payment method changed from Visa/Mastercard to bKash/Nagad — caused
  by context.md line: "Payment is mostly bKash/Nagad, rarely card"
- Animation removed — caused by: "Floor is a mid-range Android phone
  on 4G that drops to 3G indoors"
- Screenshot-friendly layout added — caused by: "they screenshot
  confirmation pages before trusting a purchase"
- Hidden fee caution added — caused by: "Trust breaks the moment a fee
  changes late in the flow"
- Mobile-first, one-hand design — caused by: "Most sessions happen on
  a shared family phone"
