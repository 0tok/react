# Methodology: modelling one person's thinking patterns

## 1. The problem

"Write down how a human thinks" is not possible as a description. A paragraph saying
"she is sarcastic and likes puns" does not let anyone predict what she would say in a new
situation. What _is_ possible is an **operational model**: a set of rules that take a
scenario as input and produce a response as output, plus a test that checks the output
against the real person.

So a thinking pattern here is defined as:

> A pattern is anything that lets a model predict this person's response to a scenario
> better than a generic model would, and that can be falsified by asking the person.

If a pattern file cannot be used to make a prediction that could be wrong, it is not done.

## 2. The three artefacts

Each person being modelled has three kinds of files. They have different jobs and
different update rules.

### 2.1 Memory (`memory.md`)

**What it holds:** facts. Biography, preferences, vocabulary, people and projects they
refer to, things they have explicitly said about themselves.

**Rule:** every entry carries a `source` (which conversation or round) and a `confidence`
(`observed` = they did it, `stated` = they said it about themselves, `inferred` = the model
guessed). Inferred entries are not allowed to influence predictions until they are
confirmed by the person.

**Why separate from patterns:** facts change without the pattern changing. A joke about a
coworker depends on _who_ the coworker is (memory) and _how_ the person jokes (pattern).

### 2.2 Patterns (`patterns/<name>.md`)

**What it holds:** one way of thinking, written as an operational model with six sections.
See `patterns/_template.md`. The sections exist because each answers a question the
model has to answer at generation time:

| Section              | Question it answers at generation time                                             |
| :------------------- | :--------------------------------------------------------------------------------- |
| Triggers             | Does this pattern fire at all in this scenario?                                    |
| Mechanism            | What transformation does the person apply to the input?                            |
| Selection            | Of all possible outputs, which one would they actually pick?                       |
| Boundaries           | What would they never do, even if it fits the mechanism?                           |
| Delivery             | What form does it take: length, tone, punctuation, language?                       |
| Calibration examples | Paired scenario → actual response, with the person's verdict on the model's guess. |

**Rule:** calibration examples are the ground truth. Every other section is a hypothesis
that must explain the examples. When a new example contradicts a rule, the rule changes,
not the example.

### 2.3 Calibration rounds (`calibration/<pattern>-round-NN.md`)

**What it holds:** one iteration of the loop below. Elicitation answers, blind
predictions, scores, and the list of pattern edits that came out of it.

## 3. The loop

```
  capture  ──►  extract  ──►  predict  ──►  score  ──►  revise
     ▲                                                     │
     └─────────────────────────────────────────────────────┘
```

### Step 1: Capture

Collect raw material. Two kinds, in order of value:

1. **Samples:** real things the person said or wrote. Messages, comments, things they
   remember saying. The more unedited, the better. Ten real samples beat a hundred
   self-descriptions.
2. **Self-report:** the person's answers to targeted questions. Useful for boundaries
   ("what would you never joke about") and for memory. Less reliable for mechanism,
   because people are bad at describing their own habits.

### Step 2: Extract

The model reads the samples and fills in the pattern sections. Each rule it writes must
cite at least one sample. A rule with no cited sample is marked `hypothesis`.

### Step 3: Predict (blind)

A **scenario battery** of 8 to 12 fresh situations is written. The person writes their
actual response to each one **first**, in a file the model has not read. Then the model
writes its prediction for each. Order matters: if the person sees the prediction first they
anchor on it and the test is worthless.

### Step 4: Score

Two scores per scenario, both given by the person:

- **Would-I-say-it** (0 to 3): 0 = not me at all, 1 = roughly my direction, 2 = close,
  I might say that, 3 = that is exactly what I would say or think.
- **Lineup** (pass/fail): the person is shown three candidates, the model's prediction and
  two decoys written in a plausible but different style, and asked which is theirs. Pass if
  they pick the model's.

Round score = mean would-I-say-it score, and lineup pass rate.

### Step 5: Revise

For every scenario scored 0 or 1, write down _why_ it missed, in one line, and which
section of the pattern was wrong. Edit that section. Add the person's real answer to the
calibration examples. Bump the round number.

## 4. Success criteria

The experiment on a single pattern is considered successful when, on a **fresh** scenario
battery the model has never seen:

| Metric              | Target |
| :------------------ | :----- |
| Mean would-I-say-it | ≥ 2.0  |
| Lineup pass rate    | ≥ 70%  |
| Rounds needed       | ≤ 5    |

If after 5 rounds the score is still below target, the pattern is either not stable in the
person (humans are not fully consistent) or the structure of the pattern file is wrong.
Both outcomes are findings. Write them down.

## 5. Things that will go wrong

- **Flattery drift.** Models tend to make the person wittier and kinder than they are.
  Counter: the lineup test. Decoys should include a "flattering" version.
- **Overfitting to the samples.** The model repeats the exact jokes from the samples.
  Counter: scenario batteries must be about new topics.
- **Self-report mismatch.** The person says "I never do X" and then does X in a sample.
  Rule: samples win. Record the mismatch in memory as a stated-vs-observed note; it is
  itself a pattern.
- **Mood.** Response depends on the person's day. Note the context when capturing, and
  accept that some scenarios will have several valid answers.
- **The model answering as itself.** Any response that is generically helpful, balanced
  or polite is a smell. The person is specific.

## 6. Adding a new pattern

1. Copy `patterns/_template.md` to `patterns/<name>.md`.
2. Write a capture questionnaire and a scenario battery in `calibration/<name>-round-01.md`.
3. Run the loop. Do not start a second pattern until the first has at least one scored
   round; the scoring process itself is what tells you whether the template works.

## 7. Reusing this for other things

The same loop works for anything where a person's response can be checked against them:
decision-making style, how they give feedback, what ideas they generate in a brainstorm,
how they write. Only the pattern sections and the scoring rubric change. Humor was chosen
first because it is the hardest to fake and the easiest to score: people know instantly
whether a joke is theirs.
