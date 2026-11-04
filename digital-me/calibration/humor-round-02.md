# Humor — calibration round 02 (lineup)

> Status: predictions written, waiting for scores on the Humor Lab page.
> **Do not read Part C before rating round 2 on the page.** It names which line is the
> prediction, and knowing that spoils the lineup.

## Design

First prediction round. For each of 12 new scenarios the page shows three lines in a
fixed, varied order:

- **pred** — written to sound like them, from the round 1b pattern.
- **flat** — flattering decoy: wittier, more built, a second beat.
- **gen** — generic decoy: what a helpful assistant would say.

They score all three 0 to 3, mark laughs, and type their own. Lineup passes when pred
scores strictly above both decoys. Targets from the methodology: pred mean ≥ 2.0, lineup
pass ≥ 70%.

Two scenarios (#5, #9) are observational with nobody addressing them; the prediction there
is silence, to test the "reactive only" trigger. One (#11) is work-adjacent self-deprecation
from a non-technical boss, to find the edge of the developer-joke boundary.

## Part C — Predictions

| #   | Scenario                                                       | pred                                                  | flat                                                                        | gen                                               |
| :-- | :------------------------------------------------------------- | :---------------------------------------------------- | :-------------------------------------------------------------------------- | :------------------------------------------------ |
| 1   | Waiter: "was everything okay?" Meal was mediocre.              | Still alive, so yes :))                               | It was fine. The bread was the main character though.                       | Yeah it was good, thanks.                         |
| 2   | Friend borrows money "until Friday", third time this month.    | Which Friday?                                         | Sure, I'll add it to the Friday collection. It's getting big.               | Again? Ok, but this is the last time.             |
| 3   | Neighbour asks about last night's noise. You were the noise.   | Yes, terrible people. Someone should talk to them.    | I did. I was also the noise. Sorry, the chair lost.                         | Sorry, that was me, had some friends over.        |
| 4   | Party: what do you think about astrology?                      | Depends which sign is asking :))                      | It's the only science where the data is stars and the results are vibes.    | Not really my thing, but fun to read sometimes.   |
| 5   | Queue, person ahead argues over 20 cents. Nobody talks to you. | (say nothing, wait)                                   | I'd pay the 20 cents just to get my life back                               | Some people, honestly.                            |
| 6   | Friend: "you've changed since you got that job."               | Hopefully for the better, but I doubt                 | I've changed into someone with a salary, mainly.                            | Have I? Didn't notice, but maybe you're right.    |
| 7   | Help me move apartments on Saturday?                           | Depends, which floor?                                 | Only if we're moving you to the ground floor.                               | Sure, what time?                                  |
| 8   | Friend's kid: why is the sky blue?                             | Nobody knows. Ask your father.                        | Because blue is the sun's favourite colour and the sun always gets its way. | It's because of how sunlight scatters in the air. |
| 9   | Group chat pizza argument, you haven't spoken.                 | (stay out of it)                                      | Settle it like adults: I'll order from all three and report back            | They're all fine, just pick one                   |
| 10  | "Do you ever get bored of your phone?"                         | Yes, but it doesn't get bored of me                   | My phone and I are in a stable, toxic relationship.                         | Sometimes. I try to leave it in another room.     |
| 11  | Non-technical boss: could the AI tool do your job?             | Already does, I just press enter                      | It could do my job. It just can't sit through my meetings, so I'm safe.     | Parts of it, probably. Not all of it yet.         |
| 12  | Compliment on your cooking. It was delivery.                   | Thanks, the hard part was choosing the restaurant :)) | Thanks. The chef sends his regards, he's three streets away.                | Haha thanks, honestly it was delivery.            |

## Part D — Scores

Scored on the page, 2026-11-03/04. Scores are 0–3 for pred / flat / gen.

| #   | pred | flat | gen | Lineup  | Laugh | Own answer               |
| :-- | :--- | :--- | :-- | :------ | :---- | :----------------------- |
| 1   | 2    | 0    | 1   | pass    |       |                          |
| 2   | 1    | 0    | –   | partial | pred  |                          |
| 3   | 0    | 1    | 2   | fail    |       |                          |
| 4   | 0    | 0    | 0   | fail    |       | Depends on who is asking |
| 5   | 1    | 0    | 0   | pass    |       |                          |
| 6   | 1    | 2    | 0   | fail    |       |                          |
| 7   | 1    | 0    | 1   | tie     |       |                          |
| 8   | 0    | 0    | 0   | fail    |       |                          |
| 9   | 0    | 0    | 0   | fail    |       |                          |
| 10  | 0    | 0    | 0   | fail    |       |                          |
| 11  | 1    | 0    | 1   | tie     | pred  |                          |
| 12  | 1    | 0    | 0   | pass    |       |                          |

**Round score:** pred mean 0.67 / 3 (target 2.0). Lineup 3 of 11 fully scored = 27%
(target 70%). Totals across all scenarios: pred 8, gen 5, flat 3. The prediction is the
best of the three on aggregate but nowhere near "exactly me".

Only one own answer was typed this round, so ground truth is thin. Round 3 fixes that in
the interface: the own answer is required before the lines are revealed.

## Part E — Misses and pattern edits

- **#4 astrology.** Pred "Depends which sign is asking :))" scored 0. Their own: "Depends
  on who is asking". Same skeleton, but the twist and the smiley killed it. Edit:
  **deflection by ambiguity** is its own mechanism; the dodge is the whole joke, add
  nothing to it. Delivery: `:))` is rare, at most one in twelve; default none.
- **#3 the noise.** Mock-sincere deflection of blame scored 0; the plain apology scored 2.
  Edit, Boundaries: when they are at fault, they own it plainly. Mock-sincere is for
  low-stakes situations (cashback, small talk), never for dodging responsibility.
- **#6 "you've changed".** Flattering decoy "I've changed into someone with a salary,
  mainly" won with 2 over vague self-doubt at 1. Edit, Selection: a concrete literal
  reframe beats vague self-deprecation. Self-deprecation needs an object.
- **#7 moving apartments, #11 AI doing your job.** Ties with the generic answer. Edit,
  Selection: when the request is real (a favour, a boss's question), the practical answer
  is at least as likely as the joke.
- **#8 kid's question, #10 bored of phone.** All three at 0, no own answer. Unknown. Retest
  with a kid question in round 3 (#5).
- **#9 pizza group chat.** Predicted silence scored 0, but "silent" was not ticked either.
  Unknown. Retest the group-chat trigger in round 3 (#6) with a direct ask.
- **#1, #5, #12 passes.** Understatement ("Still alive, so yes"), silence as a bystander,
  and mock-sincere confession all in the right direction. None scored 3.
- Interface: own answer now required before reveal.
