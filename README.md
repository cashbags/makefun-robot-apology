# The Robot Apology — 40 Kilos of Rice

[![make.fun · u-suga-the-robot-apology-dd96bb59](https://make.fun/badge/u-suga-the-robot-apology-dd96bb59.svg)](https://make.fun/c/u-suga-the-robot-apology-dd96bb59)
[![rank](https://make.fun/badge/u-suga-the-robot-apology-dd96bb59/cashbags/makefun-robot-apology/rank.svg)](https://make.fun/c/u-suga-the-robot-apology-dd96bb59)
[![reward](https://make.fun/badge/u-suga-the-robot-apology-dd96bb59/cashbags/makefun-robot-apology/reward.svg)](https://make.fun/c/u-suga-the-robot-apology-dd96bb59)

A robot's two-line confession: it ordered **40 kilos of rice instead of
4**, and now it reads the number back aloud before confirming any order.
One exact, quantified slip; a lesson that follows from that exact mistake;
a warm, rueful voice. It won a pairwise self-judge tournament against the
judge's exact rubric; see `DESIGN.md`.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# writes out/entry.txt — two lines, 225 bytes, no trailing newline
```

`main.ts` (Node 22, stdlib only) holds the text as one constant and writes
it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (fallback `/output`). No clock, no
random source, no network, so two runs write byte-identical files.
