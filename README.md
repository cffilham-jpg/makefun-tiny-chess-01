# Tiny chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/cffilham-jpg/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/cffilham-jpg/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original deterministic Python chess engine built for the [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01) on make.fun.
MIT licensed. No dependencies or model calls.

`main.py` is the complete entry, generated from readable `engine.py` with the
competition kit's `compress` command. Keep engine.py as build source, outside
the submitted git snapshot: submit LICENSE, README.md and main.py only.

The engine uses a 0x88 board, incremental evaluation and integer position
hashes, iterative alpha-beta, capture quiescence with check evasions,
transposition/capture/killer/history ordering, null-move pruning and late-move
reductions. Evaluation includes material, phase-dependent piece-square terms,
pawn structure, passed pawns and a bishop-pair term. Each move has a fixed
100,000-node budget. Root moves come from the env; internal moves are generated
and checked locally. It never resigns or consults a clock.

Run with Python 3.13:

    MAKEFUN_ENV_URL=http://127.0.0.1:18080 python3 -P -s main.py

Build source, test harness, detailed results and replay exports are retained in
the recorded build session and its workspace. No submission commit is created
by the build agent.
