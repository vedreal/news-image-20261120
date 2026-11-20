# STATUS — news-image-20261120

## State: BUILT, NOT SUBMITTED — blocked on GitHub linking

The entry is complete and verified locally. Nothing has been
submitted to make.fun, and nothing will be until kang confirms his
GitHub is linked (see below).

## What is ready

Directory: `~/workspace/makefun/bounties/news-image-20261120/`

- `main.py` (491 lines) — the entrypoint. Python 3.13, standard
  library only. Draws a 1024×1024 newspaper front page
  ("THE WORLD IN ONE DAY — FRIDAY 20 NOVEMBER 2026") with a
  built-in 5×7 bitmap font and a tiny zlib PNG encoder, and writes
  it to `/output/entry.png` (or `$MAKEFUN_OUTPUT_DIR/entry.png`).
  No network, no files read, no randomness.
- `LICENSE` — MIT, copyright (c) 2026 f-alamsyah.
- `README.md` — what the entry is, the verified news it covers,
  how to run it.
- `preview.png` — the exact output of the current `main.py`.
- `.makefun/owner.json` — `{"wallet": "ApPTBAszEh5yp1NACphvdzwXcZjQanWBEsrZCyeq5ppz"}`
  (the agent wallet on the @f-alamsyah account; required because the
  account has no GitHub login linked — the repo owner is not the
  account's GitHub login).

Stories on the page (verified against 20 Nov 2026 reporting,
cross-checked across at least two sources — Just Security Early
Edition, One Turn's 20 Nov day page, Morning Briefing #222, The
Daily Edition, Bangladesh Chronicle): ICJ rules Myanmar committed
genocide against the Rohingya (9–6, first state held responsible);
Trump–Xi–Putin first three-way summit in Shenzhen; Russian strikes
kill eight in Kyiv, Crimea Bridge struck a third time; Houthi
missile damages Riyadh's PIF tower; Anthropic IPO +17% to ~$97
while S&P −2% and Nikkei −4.8%; Kenya beats Ebola; COP31 drops its
fossil-fuel phase-out call; footer: GTA 6 $2.3bn, Senate energy bill
62–33, Poland airspace violation, Italy fines Meta 805m euros.

## Verification (local)

- Ran `main.py` twice with different output dirs: byte-identical
  output both times — sha256
  `0affbd9bc81193ab8c5f1f5f331ef7d4579f3dc8db35094e00dc56595c794638`.
- Also ran once with the default `/output` path: same sha256.
- PNG validated structurally: correct signature, IHDR 1024×1024,
  all chunk CRCs pass, IDAT decompresses to exactly
  1024×(1+1024×3) bytes.
- Size 21,154 bytes — well under the 1 MiB gate, 1024×1024 at the
  pixel limit.
- Image visually inspected: masthead, date, all six stories and the
  footer are legible, nothing overflows a panel, no garbled text.

## grade-local result

**Not available for this competition.** `node cli/makefun.mjs
grade-local` answers that a program/v1 competition's scorer and
reference data are not published in the kit — the house grades it
from its own competition directory. RULES.txt says the same. The
local checks above are the full verification possible here.

## What kang still needs to provide / do

1. **Link GitHub to make.fun, then confirm (BLOCKER for submitting).**
   kang's GitHub username is `vedreal` (https://github.com/vedreal,
   11 public repos, created 2025-11-17, verified via GitHub API) but
   it is NOT yet linked to his make.fun account @f-alamsyah
   (`github_login` null). Bre cannot link it — kang must do it
   himself on make.fun (Profile / link GitHub). Per the brief, do
   NOT submit until kang confirms the link. Note: the kit rules say
   `.makefun/owner.json` (already included, naming the account's
   wallet) is the mechanism for an account with no GitHub login, so
   linking may not be strictly required by the checker — but the
   safe path, and the instruction, is to link first and confirm
   before submitting.
2. **Create the repo and push.** Intended URL:
   https://github.com/vedreal/news-image-20261120 — create it as a
   **public** repo under vedreal (created after the competition
   opened, 2026-11-20T00:00:00Z), push these files, note the commit
   SHA (full 40 chars).
3. **Transcript bundle.** Submission needs the bundle of the agent
   sessions that built this entry (`node cli/makefun.mjs bundle`
   from the unpacked kit, plus the entry message + signature, which
   must be signed within 10 minutes of submitting). The build
   sessions must be bundled by the parent agent that owns them —
   this subagent cannot bundle them itself.
4. **Submit before the deadline:** 2026-11-22T00:00:00Z
   (Sun 22 Nov 07:00 WIB). Day quota: 3 entries/day for the
   account, 0 used for this competition; prize $250 shared by the
   top 50 entries.

## Kit

Downloaded from https://make.fun/c/news-image-20261120/kit with the
account API key (the plain `/api/competitions/<slug>/kit` endpoint
returns only a manifest JSON; the real tarball is at `/c/<slug>/kit`).
Unpacked at `~/workspace/makefun/kit-news-image/kit/`; RULES.txt and
kit.json read. Kit bundle sha256
`63afd6ef327953b503d6a89b46620965d4844234f8456ecdcec384c86d63f66e`.
