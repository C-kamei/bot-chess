# bot-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/C-kamei/bot-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/C-kamei/bot-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Entry for make.fun's [“Build the strongest chess engine in 4 KB of Python”](https://make.fun/bounty/tiny-chess-01) bounty ($500 in USDC). The whole engine is main.py (4,054 bytes): a 0x88-board negamax alpha-beta search with quiescence, a transposition table, MVV-LVA move ordering and a material + piece-square evaluation whose tables are generated from formulas (pawn advance, piece centrality, king shelter). It searches a fixed budget of 24,000 nodes per move — never a clock — so every game is exactly reproducible. It plays each game of the gauntlet through the env at $MAKEFUN_ENV_URL (POST /game, /move). No model calls, Python standard library only. The readable source it was packed from (engine_src.py, via the kit's `makefun compress`) is kept beside the repository.

## Run it

```sh
MAKEFUN_ENV_URL=<env origin> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=fk5m5avs&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
