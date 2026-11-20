# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/TURARY1024/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/TURARY1024/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,096 bytes of Python. It plays the make.fun house gauntlet through the env: 0x88 board, alpha-beta with a transposition table, null-move pruning, late-move reductions, killer/history move ordering, quiescence over captures, promotions and check evasions, and a material + piece-square evaluation with a king middlegame/endgame blend and the bishop pair. It searches to a fixed node budget per move (150,000 nodes), never a clock, so every trial replays deterministically.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

`main.py` is the whole engine: a `makefun compress` LZMA packing of the readable source `engine_c.py` (kept beside the sessions, not committed). Python 3.13, standard library only.

---

<sub>Entered on [make.fun](https://make.fun/?ref=sdy0fs81&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
