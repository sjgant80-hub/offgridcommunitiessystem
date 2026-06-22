# kcc · Konomi Cube Coin · Community OS

> A sovereign single-HTML community operating system for off-grid and intentional communities. Members · mutual-credit ledger denominated in KCC · governance · calendar · resource share · skill share. No SaaS. No subscription. No government API. Runs on a Raspberry Pi, a USB stick, or a kid's chromebook.

**Live:** https://sjgant80-hub.github.io/kcc/

## What it is

A practical day-to-day OS for a small intentional community (5 – 200 people) that wants out of government money, SaaS subscriptions, and centralised platforms — and into land-based, self-governing, value-for-value living.

You get one HTML file. Open it. Add your members. Start recording exchanges. Hold proposals. Coordinate workdays. Borrow each other's tools. Teach each other skills. The whole community fabric, in your hand.

## What KCC is

**Konomi Cube Coin** — the unit of account.

KCC isn't government money. It isn't a crypto-asset. It's a community-issued unit of mutual credit. The default peg is **1 KCC ≈ 1 hour of contributed labour**, but every community sets its own:

- *"1 KCC = 1 hour"* (time-based, simplest)
- *"1 KCC = 1 kWh of electricity contributed"* (energy-based)
- *"1 KCC = 1 kg of harvested food at the community rate"* (basket-based)
- *"1 KCC = vote of the council"* (hybrid)

The ledger tracks who owes whom how many KCC. Members can go negative within a community-set floor. There is no central bank. There is no fee. There is no third party. The cosmology of the cube (why a cube? why this name?) is its own thing and lives elsewhere — for the operator layer, KCC is simply the unit that lets you trade fairly without money.

## What you get on day one

| Module | What it does |
|---|---|
| **Members** | Directory · skills · offers · needs · contact · role · per-member KCC balance |
| **Ledger** | Every exchange recorded · double-entry · category (hours / goods / service / tool-loan / gift) · two-party acknowledgement · running balance |
| **Governance** | Proposals · voting method per proposal (consensus / majority / sociocracy / unanimous) · per-member vote · pass/fail/withdrawn states · decided-at timestamp |
| **Calendar** | Workdays · harvest days · meetings · markets · feasts · attendance |
| **Resource share** | Tools · equipment · vehicles · spaces — available to borrow within the community |
| **Skill share** | "I can teach X" / "I need help with Y" / "Looking for X" board |
| **Settings** | Community name · KCC peg definition · governance default · ledger floor |
| **Backup** | Whole-workspace JSON export · markdown export per view · cross-device import |

## What's *not* in v1 (planned as separate seeds that federate via mesh)

- **fallseed-permaculture** — zones, sectors, food-forest layers, crop rotation, companion planting
- **fallseed-livestock** — rabbits, chickens, goats, count + feed + breeding + cull records
- **fallseed-larder** — preserved food inventory, seed bank, harvest logs

When those ship, they plug into KCC via the cross-seed mesh — no new app to install, just data flowing into your existing KCC dashboard.

## Sovereignty contract

- **Your data lives in your browser's IndexedDB.** Never sent anywhere by default.
- **No analytics. No tracking. No telemetry.** Open DevTools → Network — nothing leaves your machine unless you explicitly set up mesh sync.
- **No subscription. No login. No account.** Open the page, you have it.
- **MIT-licensed.** Fork it. Modify it. Sell your fork. Whatever serves your community.
- **One file.** ~80KB. Save the HTML to a USB and it runs on any browser, offline, forever.
- **If we disappear**, the file you saved keeps working. Your community keeps running.

## Install (3 options)

### Option 1 — open in your browser (easiest)
Bookmark https://sjgant80-hub.github.io/kcc/ · install as PWA from your browser menu (Add to Home Screen) · done.

### Option 2 — save the file (most sovereign)
1. Right-click https://sjgant80-hub.github.io/kcc/ → Save Page As → `kcc.html`
2. Double-click `kcc.html` whenever you want it. Works offline. Works from a USB stick.
3. Your IndexedDB is per-origin so the saved file gets its own storage.

### Option 3 — Raspberry Pi / community server
On a Pi (or any tiny Linux box):
```bash
curl -O https://sjgant80-hub.github.io/kcc/index.html
python3 -m http.server 8080 --bind 0.0.0.0
# every member on your local network can now visit http://<pi-ip>:8080
```
The Pi can sit on a shelf in the community hall. Members hit it from phones. When the Pi is off, members still have local copies. When it's on again, everyone syncs.

### Option 4 — fork it
Fork on GitHub, edit `index.html` to suit your community, enable Pages on your fork — you have your own deployment.

## Mesh sync (optional)

By default KCC is local-first / device-local. To sync across members:

1. Each member opens KCC and runs it locally — they each have their own copy.
2. Optionally, point the mesh-URL in Settings to a shared relay — either a Cloudflare Worker (free tier handles a small community easily) or a community Raspberry Pi running a tiny sync server.
3. Members' devices push ledger entries, proposals, and events to the relay. Other members pull updates when they open KCC.

The relay never holds the data permanently — it's a forwarding bulletin board. If it disappears, everyone still has their local copy.

(The relay code is a 50-line Cloudflare Worker shipped separately. Until your community needs federation, you don't need to set anything up.)

## Tone

Practical. Dignified. Land-grounded.

Not a hippy aesthetic. Not a tech-bro aesthetic. Closer to *"1880s farmers' co-operative manual"* meets *"Linux man page"*. The tool should help you spend less time on the laptop, not more.

The best signal that KCC is working: a member closes the laptop and goes outside.

## Spec link

This seed implements the Fork Seed pattern. See https://www.ai-nativesolutions.com/spec.html for the SEED schema and cross-seed mesh protocol.

## License

MIT. See `LICENSE`.

## Built by

Simon Gant · sjgant80@gmail.com · https://www.ai-nativesolutions.com

Part of the AI Native Solutions estate. Star Trek × Hobbiton.
