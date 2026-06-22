# offgridcommunitiessystem · Off-Grid Community System

> A sovereign single-HTML community operating system for off-grid and intentional communities. Members · mutual-credit ledger · governance · calendar · resource share · skill share. No SaaS. No subscription. No government API. Runs on a Raspberry Pi, a USB stick, or a kid's chromebook.

**Live:** https://sjgant80-hub.github.io/offgridcommunitiessystem/

## What it is

A practical day-to-day OS for a small intentional community (5 – 200 people) that wants out of government money, SaaS subscriptions, and centralised platforms — and into land-based, self-governing, value-for-value living.

You get one HTML file. Open it. Add your members. Start recording exchanges. Hold proposals. Coordinate workdays. Borrow each other's tools. Teach each other skills. The whole community fabric, in your hand.

## The unit of account

The ledger is denominated in whatever your community decides. Default: **1 credit ≈ 1 hour of contributed labour**. Settings let you redefine it:

- *"1 credit = 1 hour"* (time-based, simplest)
- *"1 credit = 1 kWh of electricity contributed"* (energy-based)
- *"1 credit = 1 kg of harvested food at the community rate"* (basket-based)
- *"1 credit = a vote of the council"* (hybrid)

You give it any short label in Settings — "hours", "credits", "marks", whatever. The mechanics are mutual-credit: who owes whom how much. No central bank. No fee. No third party. Each community calibrates its own peg.

## What you get on day one

| Module | What it does |
|---|---|
| **Members** | Directory · skills · offers · needs · contact · role · per-member balance |
| **Ledger** | Every exchange recorded · double-entry · category (hours / goods / service / tool-loan / gift) · two-party acknowledgement · running balance |
| **Governance** | Proposals · voting method per proposal (consensus / majority / sociocracy / unanimous) · per-member vote · pass/fail/withdrawn states |
| **Calendar** | Workdays · harvest days · meetings · markets · feasts · attendance |
| **Resource share** | Tools · equipment · vehicles · spaces — available to borrow within the community |
| **Skill share** | "I can teach X" / "I need help with Y" / "Looking for X" board |
| **Settings** | Community name · unit definition + label · governance default · ledger floor · mesh URL · light/dark theme |
| **Backup** | Whole-workspace JSON export · cross-device import |

## What's *not* in v1 (planned as separate seeds that federate via mesh)

- **fallseed-permaculture** — zones, sectors, food-forest layers, crop rotation, companion planting
- **fallseed-livestock** — rabbits, chickens, goats, count + feed + breeding + cull records
- **fallseed-larder** — preserved food inventory, seed bank, harvest logs

## Sovereignty contract

- **Your data lives in your browser's IndexedDB.** Never sent anywhere by default.
- **No analytics. No tracking. No telemetry.** Open DevTools → Network — nothing leaves your machine.
- **No subscription. No login. No account.**
- **MIT-licensed.** Fork it. Modify it. Sell your fork.
- **One file.** ~80KB. System fonts only — zero CDN dependencies. Save it to a USB and it runs offline forever.
- **If we disappear**, the file you saved keeps working.

## Install

### Option 1 — open in your browser (easiest)
Bookmark https://sjgant80-hub.github.io/offgridcommunitiessystem/ · install as PWA from your browser menu.

### Option 2 — save the file (most sovereign)
1. Right-click the page → Save Page As → `community.html`
2. Double-click whenever you want. Works offline. Works from a USB stick.

### Option 3 — Raspberry Pi / community server
```bash
curl -O https://sjgant80-hub.github.io/offgridcommunitiessystem/index.html
python3 -m http.server 8080 --bind 0.0.0.0
# every member on your local network visits http://<pi-ip>:8080
```

### Option 4 — fork it
Fork on GitHub, edit `index.html`, enable Pages on your fork.

## Tone

Practical. Dignified. Land-grounded.

Not a hippy aesthetic. Not a tech-bro aesthetic. Closer to *"1880s farmers' co-operative manual"* meets *"Linux man page"*. The tool should help you spend less time on the laptop, not more.

The best signal it's working: a member closes the laptop and goes outside.

## License

MIT.

## Built by

Simon Gant · sjgant80@gmail.com · https://www.ai-nativesolutions.com

Part of the AI Native Solutions estate. Star Trek × Hobbiton.
