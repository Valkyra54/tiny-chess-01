# tiny-chess-01 v1

Original chess engine (MIT). Rotating-board negamax with alpha-beta,
iterative deepening to a fixed 75,000-node budget, quiescence, transposition
table, killer/history ordering, and an eval with material, piece-square
tables, bishop pair, passed pawns, rook bonuses and king safety. Packed
with LZMA + base85 into `main.py` (4,091 bytes).

## Results

Practice trials on the local env server, 16 games each, all Elo 1464:

- Trial 0: 6 wins, 6 draws, 4 losses
- Trial 1: 8 wins, 2 draws, 6 losses
- Trial 2: 7 wins, 4 draws, 5 losses

Mean Elo 1464 vs the 1,360 sunfish house baseline (+104). Design: negamax
alpha-beta with PVS, iterative deepening to a fixed 75,000-node budget,
quiescence, transposition table, killer/history ordering; packed with LZMA
+ base85 into `main.py` (4,091 bytes). Mean move ~2.75 s, slowest ~4.4 s
(limit 10 s/move), 0 timeouts in 2,165 move calls. Deterministic: fixed
node budget, no clock, no randomness.
