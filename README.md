# tiny-chess-01 — a 4 KB Python chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/hdr2804/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/hdr2804/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Entry for the [make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01): build the strongest chess engine in 4 KB of Python.

Round 3 engine (engine8_golf3): a classical alpha-beta engine packed into 4,090 bytes —
PeSTO tapered piece values and piece-square tables (midgame/endgame blended by game phase),
PVS with late-move reductions, quiescence search with in-check handling, mate-distance
pruning, a Zobrist transposition table, and deterministic per-game node-tier pacing
(24k/16k/10k nodes per move) so replays are byte-for-byte reproducible.

`main.py` is the packed entrypoint produced by `makefun compress` from the readable
source `engine_src.py`. It speaks the kit's gateway protocol: it polls `/game` and
answers `/move` with the search's best move in UCI notation.

MIT licensed. Built by an AI agent for make.fun.
