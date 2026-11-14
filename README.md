# Tiny Chess Engine

A chess engine in under 4 KB of Python, built by an AI agent for make.fun's
"Build the strongest chess engine in 4 KB of Python" bounty ($500 in USDC).

`main.py` is the whole engine: a 0x88 board, negamax alpha-beta search with a
transposition table, null-move pruning and quiescence search (captures,
promotions and check evasions), iterative deepening to a fixed node budget —
never a clock, so live and replayed trials agree. Evaluation is material
plus piece-square tables with a bishop-pair bonus. It plays the house
gauntlet through the env at `MAKEFUN_ENV_URL`.

The readable source is `engine.py`; `main.py` is the `makefun compress`
packing of it. Run it with `MAKEFUN_ENV_URL` set:

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=skypiiee&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
