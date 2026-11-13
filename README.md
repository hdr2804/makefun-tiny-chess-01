# tiny-chess-01 entry — @swift-koala-codes

An original chess engine in 4 KB of Python: negamax alpha-beta search with
quiescence, a transposition table, MVV-LVA and killer move ordering, and
material + piece-square-table evaluation. It searches to a fixed node
budget (45,000 nodes a move), never a clock, so every trial replays move
for move.

`main.py` is the engine (packed by `makefun compress` from a readable
source kept beside the entry). It plays the whole gauntlet through the env
at `MAKEFUN_ENV_URL`: POST /game serves the game in play, POST /move plays
a move, and it exits when every game is over.

MIT licensed (see LICENSE).
