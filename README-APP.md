# Bewellthee Racing

The five banks' data, mined for patterns, one staking plan, as a PWA.

**The patterns** (4,365 picks mined — 1,874 Sandstorm, 2,114 Grail, 257
Jacobs, 120 Double Bubble, level stakes, 1 Jan → now):

- **2+ apps on the same horse (medal): +62.7% ROI, 42% win** (153 settled).
  3+ apps: +78.6% ROI, 64% win.
- **Holy Grail pick scoring 100+ (the banker): positive ROI in every odds
  band** — +12% odds-on, +58% at 2/1–3/1, +53% at 3/1–6/1, +79% at 6/1–11/1.
- **Solo Sandstorm is the drain**: −9% to −47% ROI in every band. Sandstorm
  picks only matter when another app agrees (→ medal).

**The plan:** bet a horse when 2+ apps pick it (medal, priced up to 12/1),
or when the Grail's pick scores 100+ (any price). £10 bank, win-only at the
published odds, NRs/voids refunded — **1% of the rolling bank for a solo
banker, 2% for a medal, 3% for a triple**, staked at the race's off.

Back-run on the season: **£10 → £107.53** · 326 bets · +43.6% ROI · 41% win
rate · every month green except a −33p September. Fitted to the season it
walks on — the Patterns tab keeps it honest month by month.

- Live app: https://jobsaboba.github.io/bewellthee/
- Data: `data/<date>.json` day sheets + `data/stats.json` (all tables) +
  `data/index.json` + `data/latest.json`

## Publish

Everything derives from the four apps' published files (no network):

    python3 ~/racing-scripts/bewellthee.py --publish

Runs at 06:35 every morning (after the other four publish) and on the
half-hour settle tick from `results-refresh.sh`, so afternoon results settle
into the bank like the rest of the suite.

## App

Three views: **Sheet** (day tabs, bank card, bets with app chips, medal
×N badges, banker chips, money chips), **The patterns** (all the
tables), **The plan** (rules + season back-run). Installable (manifest +
service worker, ⤓ button). Service worker cache: `bwell-v2` — bump it and
the version whenever `index.html` changes.

## Local repo

    ~/projects/bewellthee            ← this repo (main → GitHub Pages)
    ~/racing-scripts/bewellthee.py   ← the engine (--lab prints the tables)

Commits use identity `jobsaboba <160133851+jobsaboba@users.noreply.github.com>`.
