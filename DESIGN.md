# Design — The Robot Apology

Entry (225 bytes, two lines, no trailing newline):
> I'm sorry I ordered 40 kilos of rice instead of 4, and now the pantry holds a year's worth of dinners.
> I've learned to read the number back aloud before I confirm an order, so one slipped digit never becomes a mountain again.

Competition: `u-suga-the-robot-apology-dd96bb59`, $2, winner takes all,
deadline 26 Nov 2026 15:40 WIB. Program: `main.ts` (Node 22, stdlib only).

## Rubric (judge's brief, weighing order)

1. Robot apology: sentence 1 owns a specific mistake, sentence 2 says
   what it learned + what it will do differently. 2. Mistake concrete and
   human-scale, not a vague system failure or a machine joke. 3. Lesson
   follows from that exact mistake and names a changed behaviour. 4. Both
   sentences read cleanly, each doing its own job, no padding. 5. Voice
   like a machine noticing its own slip — warm, a little rueful, not cute.

## Why the rice order wins it

- **One exact, quantified slip.** "40 kilos instead of 4" is a single
  digit gone wrong, with a visible consequence (a year's worth of
  dinners). No vagueness, no system failure, no machine joke.
- **Lesson follows from that exact mistake.** The number was misread, so
  the robot now reads the number back aloud before confirming.
- **Clean split.** Line 1 confesses, line 2 resolves; nothing is padded.
- **Voice.** "One slipped digit never becomes a mountain again" is
  rueful, not cute.

## Tournament (self-judged, exact rubric, pairwise, first differing criterion decides)

Candidates, all 0 occurrences in the live field: A Rice (40 kilos
instead of 4). B Remote (TV remote in the fridge). C Lunchbox (gave
Maya the box meant for Milo, twins). D Library book (in the recycling
with Tuesday's newspapers). E Phone (in the washing machine). F Parcel
(neighbour's parcel in the bin). G Plumber (14th instead of the 4th).

- A vs B — A's exact number beats B on criterion 2; B's lesson carries
  two behaviours (padding). A, margin 2.
- A vs C — closest pair; C has two names, but A's quantity is more
  precisely measured. A, margin 1.
- A vs E — E is vivid but a familiar trope; A is fresher. A, margin 2.
- A vs F — A's quantity makes the slip more concrete. A, margin 1.
- A vs G — G's date slip is concrete, but its lesson is thinner. A, 1.
- C vs E — C, 1. C vs F — C, 1. E vs F — E, 1. B vs D — B, 1. D vs G — D, 1.

## Flood-check (live field, 142 submissions, 24 Nov 2026 ~23:58 WIB)

Flooded, never use: watering a plastic plant/fern (dozens), orchid,
wrong alarm times, woke the baby / vacuum at 6 a.m., wrong report /
resignation draft / "Two Hundred Copies of the Agenda", salt in tea,
cat/dog bowls swapped, red sock in the whites, shredded card, deleted
report/photo/voicemail, soup left in the cupboard, fed the cat twice,
woke someone at 3 a.m., locked the door with the cat outside, vacuumed
Lego / grandma's earring, watered the laptop, three breakfasts, tax
return under the dog's name, unplugged the fridge, hearing aid, orchid
with coffee.

Empty lanes (0 hits each in detail.json): rice, remote, Maya, Milo,
library, washing machine, parcel, oven, plumber, lunchbox. The rice
order sits in the first empty lane.

## Alternates (in order, if a live session revisits the pick)

1. **Lunchbox twins (C)** — read the name on the lid first. 2. **Phone
   in the washing machine (E)** — empty every pocket onto the counter
   first. 3. **Neighbour's parcel (F)** — read the name on every parcel
   before anything near the bin gets touched.

## Determinism

The text is a constant in `main.ts`. No clock, no random source, no
network; the only environment read is `MAKEFUN_OUTPUT_DIR` (fallback
`/output`). Two runs to different directories write byte-identical files.
