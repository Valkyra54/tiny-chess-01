# tiny-chess-01 v1

Original chess engine (MIT). Rotating-board negamax with alpha-beta,
iterative deepening to a fixed 75,000-node budget, quiescence, transposition
table, killer/history ordering, and an eval with material, piece-square
tables, bishop pair, passed pawns, rook bonuses and king safety. Packed
with LZMA + base85 into `main.py` (4,047 bytes).

Practice trials (local env server, 16 games each): Elo 1464 on trials 0,
1 and 2 (mean 1464 vs the 1,360 house baseline). Mean move time ~2.75 s,
slowest ~4.4 s (limit 10 s/move). Deterministic: fixed node budget,
no clock, no randomness.
