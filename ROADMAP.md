# DashCalc — Apple App Development Roadmap

**Project:** DashCalc — voice-first gig delivery profitability calculator
**Owner:** NobleLogic LLC (NobleLogic1)
**Status:** Web app built, roadmap defined, not yet started on native build
**Last updated:** October 10, 2026

---

## Overview

DashCalc is a hands-free calculator for gig delivery drivers (DoorDash, Uber Eats, etc.). The driver speaks an order — pay, miles, time — and the app returns profit per delivery and effective hourly rate, accounting for fuel cost and vehicle wear.

**Core formula:**

```
Profit per delivery = Pay − (Miles ÷ MPG × Gas Price) − (Miles × Wear Rate)
Effective hourly rate = Total pay ÷ Total hours worked (including deadhead miles)
```

**Default settings:**
- Wear rate: $0.20/mile (tires, oil, brakes, depreciation)
- MPG and gas price: user-configurable, remembered between sessions

**Tech stack (current):** Single-file HTML web app — speech-to-text input, calculation logic, text-to-speech output. Works in mobile browser.

---

## Phase 1 — Polish the Web App (Weeks 1–4)

- Fix voice parsing edge cases (messy spoken input, partial orders)
- Add delivery history log (per-shift and cumulative stats)
- Offline support — drivers lose signal in parking garages
- Test on real shifts with real orders

## Phase 2 — Capacitor Wrap (Weeks 5–8)

- **Requirement:** Mac with Xcode (free from the App Store)
- Wrap existing HTML in Capacitor — native shell, home screen icon, full-screen mode
- Add native plugins: microphone access, background audio for between-order listening
- Code barely changes; Capacitor packages it as a native iOS binary

## Phase 3 — App Store Prep (Weeks 9–12)

- Apple Developer Program: $99/year (required for distribution beyond own device)
- Privacy policy URL (required — app uses the microphone)
- App Store listing: name, subtitle, description, screenshots (multiple iPhone sizes), category (Business or Utilities)
- Submit for review: expect a few days to two weeks; first-pass rejection is common (usually a missing privacy label)

## Phase 4 — Real Product (Months 4–6)

- Pull order data automatically from DoorDash / Uber Eats APIs instead of spoken input
- This is the version drivers pay for — zero manual entry
- Much larger build than phases 1–3

## Phase 5 — Iterate (Ongoing)

- Updates go through the same review process, faster for bug fixes
- Real driver feedback drives what to fix next

---

## Costs

| Item | Cost |
|------|------|
| Apple Developer Program | $99/year |
| Mac + Xcode | Free |
| Capacitor | Free, open source |

## Timeline Summary

- Phases 1–3: roughly one month of part-time work
- Phase 4: where it becomes a business instead of a hobby
- Total to shipped App Store listing: ~4–6 months

---

## Next Actions

1. [ ] Make dashcalc repo private (Settings → General → Danger Zone → Change visibility)
2. [ ] Polish web app: delivery history + offline support
3. [ ] Get a Mac / confirm Xcode access for Phase 2
4. [ ] Draft privacy policy
5. [ ] Enroll in Apple Developer Program when ready for distribution
