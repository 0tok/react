# Humor — calibration round 03 (own answer first, then lineup)

> Status: predictions written, waiting for scores on the Humor Lab page.
> **Do not read Part C before rating round 3 on the page.**

## Design

Same lineup as round 2, with two changes from its misses:

1. The page now requires their own answer (or "I'd say nothing") before revealing the
   three lines, so every scenario yields ground truth and the lineup cannot anchor them.
2. Predictions are plainer: no smileys, no twist on a deflection, concrete objects in
   self-deprecation, honest admission when at fault, practical answers where the request
   is real. Targets unchanged: pred mean ≥ 2.0, lineup ≥ 70%.

Retests: #5 a kid's question (round 2 #8 was all zeros); #6 a group chat with a direct
ask (round 2 #9 unknown); #7 a stranger with a trivial request, where the prediction is no
joke at all; #2 and #11 being at fault.

## Part C — Predictions

| #   | Scenario                                                     | pred                                                  | flat                                                         | gen                                           |
| :-- | :----------------------------------------------------------- | :---------------------------------------------------- | :----------------------------------------------------------- | :-------------------------------------------- |
| 1   | Friend: "why are you always on your phone?"                  | Depends what you call always                          | I'm not on my phone. My phone is on me.                      | Yeah, I should cut down honestly              |
| 2   | Forgot a friend's birthday; "thanks for the birthday wishes" | Sorry, I'm bad with dates. Happy birthday, with delay | I was going for the Hollywood late entrance. Happy birthday. | Oh no, I'm so sorry! Happy belated birthday!! |
| 3   | Colleague: "what do you even do all day?"                    | Less than it looks                                    | I move pixels around and call it architecture.               | Lots of meetings and some building, honestly. |
| 4   | "You look tired."                                            | Thanks, I worked hard on it                           | It's not tiredness, it's a lifestyle.                        | Yeah, didn't sleep well.                      |
| 5   | Friend's kid: "are you rich?"                                | Not yet                                               | Rich in experience. So, no.                                  | No, but I'm doing okay.                       |
| 6   | Group chat: "who's in for Saturday?"                         | Depends who else is in                                | In, unless it's a surprise birthday. Then out.               | I'm in!                                       |
| 7   | Stranger on the bus: is this seat free?                      | (move the bag) Yes                                    | It's free, but it has opinions.                              | Yes, go ahead                                 |
| 8   | Friend wants you to watch a 40-minute video now              | Is there a short version?                             | Forty minutes? I don't have that kind of commitment in me.   | Send it, I'll watch it later                  |
| 9   | Small talk: "how's life?"                                    | Still going                                           | Life's good. Mostly a loading screen, but good.              | Good, busy. You?                              |
| 10  | Aunt: "when are you getting married?"                        | When someone agrees                                   | I'm waiting for the right person and the right deposit.      | Haha, no plans yet.                           |
| 11  | Wrong group chat; "wrong chat?"                              | Yes, pretend you didn't see                           | No, this was for you. Consider yourself informed.            | Oops, sorry, wrong chat!                      |
| 12  | "I don't get your humor."                                    | Me neither                                            | It's an acquired taste. Very few have acquired it.           | Haha fair, it's pretty dry.                   |

## Part D — Scores

Scored on the page, 2026-11-04. Own answers were typed in 10 of 12 scenarios, which is
the point of this round. The lineup was mostly skipped after the reveal (6 of 12 never
revealed, 3 scored), so lineup numbers are indicative only.

| #   | Own answer                                  | Silent | Lineup scores (pred / flat / gen)   |
| :-- | :------------------------------------------ | :----- | :---------------------------------- |
| 1   | I'm working, i have to become rich          |        | not scored                          |
| 2   | Angels told you that? I was preying for you |        | 1 / 0 / 0, pass                     |
| 3   | Waiting for salary                          |        | 0 / 0 / 0, fail                     |
| 4   |                                             | yes    | not scored                          |
| 5   |                                             | yes    | pred "Not yet" 2, others not scored |
| 6   | Ok                                          |        | not revealed                        |
| 7   | Sure it's free                              |        | not revealed                        |
| 8   | I need spoiler to consider watching         |        | not revealed                        |
| 9   | It's fine                                   |        | not revealed                        |
| 10  | Before 30                                   |        | not revealed                        |
| 11  |                                             | yes    | gen 1, pred not scored              |
| 12  | Art is not for everybody                    |        | not revealed                        |

**Round score:** pred mean 1.0 / 3 over the 3 scored (target 2.0); lineup 1 of 2 fully
scored. Too thin to count. The own answers are the result.

Comparing own answers to predictions by hand:

| #   | Pred                                                  | Own                                         | Verdict                                                                |
| :-- | :---------------------------------------------------- | :------------------------------------------ | :--------------------------------------------------------------------- |
| 1   | Depends what you call always                          | I'm working, i have to become rich          | wrong mechanism: they go grand, not evasive                            |
| 2   | Sorry, I'm bad with dates. Happy birthday, with delay | Angels told you that? I was preying for you | wrong: with a friend's dig they counter with a cover story, no apology |
| 3   | Less than it looks                                    | Waiting for salary                          | right register, wrong object: money, not modesty                       |
| 4   | Thanks, I worked hard on it                           | (silent)                                    | wrong: a statement, not a question, gets nothing                       |
| 5   | Not yet                                               | (silent), "Not yet" scored 2                | close                                                                  |
| 6   | Depends who else is in                                | Ok                                          | wrong: logistics get a plain answer                                    |
| 7   | (move the bag) Yes                                    | Sure it's free                              | right: no joke                                                         |
| 8   | Is there a short version?                             | I need spoiler to consider watching         | right direction: a condition as the dodge                              |
| 9   | Still going                                           | It's fine                                   | right register                                                         |
| 10  | When someone agrees                                   | Before 30                                   | wrong direction: a confident number, not self-deprecation              |
| 11  | Yes, pretend you didn't see                           | (silent)                                    | wrong: silence when caught                                             |
| 12  | Me neither                                            | Art is not for everybody                    | wrong direction: they go up, not down                                  |

Roughly 4 right, 8 wrong. The misses share one cause.

## Part E — Pattern edits from this round

- **Mechanism, major correction.** The dominant move is **mock-grandiosity**, not
  self-deprecation: a flat, confident, slightly grand claim in a mundane situation. "I have
  to become rich", "Art is not for everybody", "I was praying for you", "Before 30". The
  earlier self-deprecating samples (round 1b #4) are the minority. Mechanism list reordered.
- **Favourite object: money and ambition.** Rich, salary, before 30, money problems. Four of
  the 22 own answers so far. Use it as the default object for a mock-grandiose line.
- **Trigger refined.** Questions and digs get a reply. Flat statements ("you look tired")
  get silence. Logistics ("who's in", "is the seat free") get a plain answer.
- **At fault, refined.** A friend's sarcastic dig gets a counter cover story (birthday).
  Being caught without a dig (wrong chat) gets silence. A stranger's real complaint
  (round 2 noise) gets an apology. The joke is a response to provocation, never a shield.
- **Delivery.** No smileys in 10 of 10. Short: median 3 words. Occasional question opener
  ("Angels told you that?"). Non-native phrasing continues ("I need spoiler").
- **Interface.** Scoring three lines after typing an answer was skipped. Round 4 replaces it
  with one tap: pick the closest line, then optionally how close.
