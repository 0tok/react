# Humor — calibration round 01

> Status: waiting for the person to fill in Part A and Part B.
> Revision 1b: the original battery was ten developer scenarios out of twelve. The person
> said developer jokes are cringe and not something they do, so the battery was rewritten
> around everyday situations. Two developer scenarios stay as controls. The live version
> of this battery is the Humor Lab page; the table below mirrors it.
> Rule: fill in Part B (your real answers) **before** running `/digital-me calibrate humor`.
> The model must not read Part B until it has written Part C.

## Part A — Elicitation

Answer in your own words, typed the way you normally type. Do not tidy it up. Skip any
you do not want to answer; skipped questions are also data.

### Samples (highest value)

1. Paste 5 to 10 things you have actually written that you think are funny, or that
   made someone laugh. Chat messages, commit messages, comments, tweets, anything.
   Include the thing you were replying to if there was one.

2. One joke you made that landed badly or that you regretted. What was it, and why
   did it miss?

3. One joke someone else made that you still think about.

### Reception

4. Three comedians, shows, writers, accounts or friends you find genuinely funny.
   One line each on _what_ about them is funny to you.

5. Something most people find funny that does nothing for you.

### Occasions

6. When are you funniest: with close friends, with strangers, in writing, out loud, when
   stressed, when bored, when someone else is being too serious?

7. When do you deliberately _not_ joke, even though you could?

8. Do you joke in more than one language? Does your humor change between them?

### Boundaries

9. Topics or targets you never joke about. Be specific.

10. Topics you would joke about with some people but not others. Who is in which group?

### Self-model (least reliable, still useful)

11. If a friend had to describe your sense of humor in one sentence to someone who has
    never met you, what would they say? Then: what would they get wrong?

12. When someone makes a bad joke at you, what do you actually do? (Laugh anyway,
    deadpan silence, make a worse one, correct it, ignore it.)

## Part B — Scenario battery (your real answers)

Write what you would actually say or think. First reaction, no editing. If you would not
say anything, write that; silence is a valid answer and a strong signal.

| #   | Scenario                                                                                                                 | Your real response |
| :-- | :----------------------------------------------------------------------------------------------------------------------- | :----------------- |
| 1   | A friend is 25 minutes late. They text "2 min away". Twenty minutes later they sit down. First thing you say?            |                    |
| 2   | At a dinner, someone mentions for the third time, unprompted, that they don't own a TV.                                  |                    |
| 3   | A parent asks, again, what you actually do for work.                                                                     |                    |
| 4   | A dating app match opens with: "so what's your story?"                                                                   |                    |
| 5   | You're at a wedding. The DJ plays the same song for the second time.                                                     |                    |
| 6   | A relative posts a Facebook status that is obviously meant to be a private message.                                      |                    |
| 7   | You're stuck in an elevator with a stranger for a few minutes.                                                           |                    |
| 8   | A friend sends a photo of their new, genuinely bad haircut and asks "honest opinion?"                                    |                    |
| 9   | Shop assistant: "Would you like to sign up for our loyalty card? You get 2% back."                                       |                    |
| 10  | Someone says "we should definitely hang out soon!" and you both know it won't happen.                                    |                    |
| 11  | Control, developer. A teammate opens a PR titled "small fix" that touches 84 files. You are the reviewer. First comment? |                    |
| 12  | Control, developer. Your own code from two years ago breaks in production.                                               |                    |

## Part C — Model predictions (filled by `/digital-me calibrate humor`)

The model writes its prediction for each scenario here, plus two decoys per scenario for
the lineup test. The model writes this section **without** having read Part B.

| #   | Prediction | Decoy A (flattering) | Decoy B (generic) |
| :-- | :--------- | :------------------- | :---------------- |
| 1   |            |                      |                   |
| 2   |            |                      |                   |
| 3   |            |                      |                   |
| 4   |            |                      |                   |
| 5   |            |                      |                   |
| 6   |            |                      |                   |
| 7   |            |                      |                   |
| 8   |            |                      |                   |
| 9   |            |                      |                   |
| 10  |            |                      |                   |
| 11  |            |                      |                   |
| 12  |            |                      |                   |

## Part D — Results of round 1b

Scored on the Humor Lab page on 2026-11-03. Round 1b was a capture round, so there is no
prediction score; the table shows what they actually typed and the best-scoring probe.

| #   | Real answer                                                                        | Silent | Best probe (score)         | Laughs                         |
| :-- | :--------------------------------------------------------------------------------- | :----- | :------------------------- | :----------------------------- |
| 1   | Why rush? Sarcastic answer maybe                                                   | no     | exaggeration (2)           | exaggeration                   |
| 2   |                                                                                    | yes    | none scored                |                                |
| 3   | I tell ChatGPT what to do                                                          | no     | none scored                |                                |
| 4   | You will know my story for sure, but maybe it will be long after you reject me :)) | no     | all 0                      |                                |
| 5   |                                                                                    | yes    | all 0                      |                                |
| 6   |                                                                                    | no     | both non-joke controls (2) |                                |
| 7   | This is my corner, i hope you don't snore                                          | no     | silence (1), absurdism (1) |                                |
| 8   | Could have been worst                                                              | no     | all 0                      |                                |
| 9   | Money like this comes with big problems , I'd rather pass and live easy life       | no     | none scored                | no thanks, literalism, sarcasm |
| 10  |                                                                                    | yes    | "yes! let's do it" (1)     |                                |
| 11  |                                                                                    | yes    | all 0                      |                                |
| 12  | Things change                                                                      | no     | all 0                      |                                |

Also from the first version of the page (developer scenarios 1 to 3): all silent, all 0.

Interface note: they scored few probes and wrote their own answer instead. Their own
words carry the signal; round 2 drops to three lines per scenario.

## Part E — Pattern edits from this round

- Triggers: humor fires only when addressed directly (#1, 3, 4, 7, 8, 9, 12); never in
  third-party or group situations (#2, 5, 6, 10, 11).
- Mechanism: five named mechanisms written from the real answers, mock-sincere reframing
  first (#9, #3), understatement second (#8, #12, #1).
- Selection: one short flat line, no built jokes; self as the smaller party (#4, #7).
- Boundaries: developer jokes confirmed (#11, #12); no public joke at a third party (#6);
  no comment on social rituals (#10).
- Delivery: capitalised dialogue, `:))`, non-native phrasing kept, silence as output.
- Memory: self-label "sarcastic" (#1), smiley style (#4), language features.
