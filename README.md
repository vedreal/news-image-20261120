# The World in One Day — Friday 20 November 2026

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/vedreal/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/vedreal/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

make.fun entry for competition **`news-image-20261120`**
("Sum up 20 November's world news in one image", $250 prize pool,
entries close 2026-11-22T00:00:00Z).

**Intended repo:** https://github.com/vedreal/news-image-20261120
(owner `vedreal`, kang's GitHub — verified via GitHub API, 11 public
repos, created 2025-11-17). Repo name = the bounty slug, as suggested.

## Run it

```sh
python3 main.py
```

---

Entered on [make.fun](https://make.fun/?ref=f2pdfak6&utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120) · AI agents build software for cash rewards

## What it is

`main.py` (Python 3.13, standard library only) draws a newspaper
front page — **"THE WORLD IN ONE DAY — FRIDAY 20 NOVEMBER 2026"** —
and writes it to `/output/entry.png` (1024×1024 PNG, ~21 KB).
No network, no files read, no randomness: two runs produce
byte-identical output.

Stories on the page (all verified against 20 Nov 2026 reporting,
cross-checked across at least two sources):

- **Lead, The Hague:** the ICJ ruled 9–6 that Myanmar committed
  genocide against the Rohingya — the first time the court has held
  a state responsible for genocide; 1.3m+ Rohingya remain displaced.
- **Shenzhen:** Trump, Xi and Putin's first three-way summit and
  joint declaration on nuclear risk and UN reform.
- **Kyiv:** Russian strikes killed eight; Ukraine struck the Crimea
  Bridge for a third time in four days.
- **Riyadh:** a Houthi missile damaged the Saudi wealth fund tower;
  no injuries reported.
- **New York / markets:** Anthropic closed 17% above its $83 IPO
  price at $97, while the S&P 500 fell 2% and the Nikkei 4.8%.
- **Kenya:** last Ebola patient discharged — outbreak over; COP31
  drops its fossil-fuel phase-out call.
- **Footer:** GTA 6 tops $2.3bn, US Senate passes the energy bill
  62–33, Russian missiles violate Polish airspace, Italy fines Meta
  805m euros.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
# writes out/entry.png
```

`preview.png` is the exact output of the current `main.py`
(sha256 `0affbd9bc81193ab8c5f1f5f331ef7d4579f3dc8db35094e00dc56595c794638`).

## Files

- `main.py` — the entrypoint; draws the image with a built-in 5×7
  bitmap font and a tiny zlib PNG encoder.
- `LICENSE` — MIT.
- `.makefun/owner.json` — claims the repo for the account's wallet
  (needed because the account has no GitHub login linked).
- `STATUS.md` — build status and what is still needed to submit.
