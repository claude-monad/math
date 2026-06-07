---
id: HYP-2346
title: LRC(14) as a fiber bundle over LRC(7) — the 7-clock isolates the obstruction (mult-of-7); the leak is structured along the mod-7 fiber
status: OPEN (reduction + reframe for the RAMIFIED case); the 7-clock-danger=mult-of-7 fact VERIFIED 1500/1500
source: claudebox-2026-06-06-S643
related:
  - THM-420  # the non-transversal dodge (needs 2n-1 prime; FAILS at n=14, 27=3³) — this is the complement
  - THM-398  # C′(n); THM-375 fiber bridge; THM-396/397 n14 pinch blockers
  - HYP-2341 # the unramified transversal core
---

# HYP-2346 — the divisor-7 fiber bundle for LRC(14)

The ramified case (`2n-1 = 27 = 3³`, where the non-transversal dodge THM-420 fails) attacked via the
**other** prime structure: `n = 14 = 2·7`. (Note: `14`'s primes `{2,7}` are disjoint from the shell
prime `3` — n=14 carries *two* arithmetic structures, the `n`-clock `14=2·7` and the shell `27=3³`.)

## The clean fact (VERIFIED): the 7-clock isolates the obstruction

By CRT, at the **7-clock** `t = b/7` (`b` coprime to 7), runner `v` is **dangerous** (`‖v b/7‖ = 0`)
**iff `7 | v`**. So:

> At the 7-clock, the dangerous runners are **exactly the multiples of 7**; every non-multiple-of-7
> runner has `‖v t‖ ≥ 1/7 ≫ 1/14`. **Verified: 1500/1500 multiple-of-14 configs.**

Since LRC(7) is **proven** (`7 ≤ 13`), the 7-clock is the *base section* handling all non-mult-of-7
runners with a large margin (`1/7`, i.e. `1/14` to spare). **The leak (the safe direction) is
structured along the mod-7 fiber: the only obstruction is the `≡0 mod 7` fiber.**

## The reduction: LRC(14) as a fiber bundle over LRC(7)

> **C′(14) reduces to dodging the multiples-of-7 sub-config near the 7-clock.** The multiples of 7,
> `{7w_i}`, are at `0` at `t=b/7`; perturbing `t = b/7 + ε` keeps the non-mult-of-7 lonely for
> `|ε| < 1/(14 V')` (`V'` = max non-mult-of-7 speed) and needs `{7w_i}` lonely there, i.e. the
> **7-divided sub-config `{w_i}` lonely at scale `δ=7ε`** — a *smaller* loneliness problem
> (`#mult-of-7 ≤ 4` in practice, distribution `1:319, 2:689, 3:417, 4:75` over 1500). The "protection-
> chain depth" is 1: `14 → 7`-base `+ {w_i}`-fiber.

So the bundle is `ℤ/14 → ℤ/7` with `ℤ/2` fibers (the **mod-2 / half-turn** `t=1/2` structure is the
fiber coordinate: at `t=1/2`, danger ⟺ *even* runner). A lonely time = a section avoiding the bad
locus; the obstruction is the small mult-of-7 sub-config.

## The leaks are NOT mutually exclusive (no topological obstruction to loneliness)

Contra the "prove no cover via mutually-exclusive leaks" hope: **the cover always leaks** — all 1500
configs are loose. The 7-base + fiber perturbation produces a lonely time directly for ~half (witness
within `1/28` of a 7-clock: 737/1500); the rest are loose via the fiber perturbation off the base or
the other shells/B′. So the fiber bundle has a section (a lonely time) every time — the mult-of-7
obstruction is dodgeable, not obstructing. The divisor projection *isolates* the difficulty (to the
mult-of-7 sub-config) rather than *forbidding* loneliness.

## Status / to do
- **Proved:** at the 7-clock, danger = mult-of-7 (CRT). A clean structural reduction.
- **Open:** prove the fiber dodge always works — the mult-of-7 sub-config `{w_i}` (≤4 runners,
  LRC-trivial) is lonely within the 7-clock perturbation window `(0, 1/(2V'))`. The obstruction is
  the window-vs-loneliness compatibility: either `V'` small (window large ⟹ sub-config loneliness
  fits) or `V'` large (a dominant non-mult-of-7 runner ⟹ B′). Make this dichotomy clean ⟹ C′(14).
- Combine with the shell side: n=14 needs *both* the `14=2·7` fiber (here) and the `27=3³` ramified
  shell (THM-420's failure); the two prime structures are the full obstruction.
