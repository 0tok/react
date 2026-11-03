# Digital Me

An experiment in building a model of one specific person's thinking, so that an AI can
answer questions the way they would, and come up with the ideas that would occur to them
in a given scenario.

This is not a chatbot persona. The goal is predictive accuracy: given a scenario, produce
what _this person_ would actually say or think, verified against the real person.

## Layout

| Path                                    | What it is                                                                                                                |
| :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------ |
| `methodology.md`                        | How the experiment runs, how success is measured, how to add a new pattern. Reusable for other people and other patterns. |
| `memory.md`                             | Durable facts about the person. Every entry has a source and a confidence.                                                |
| `patterns/_template.md`                 | The blank structure every thinking pattern follows.                                                                       |
| `patterns/humor.md`                     | First pattern: humor. Currently a capture scaffold with a few unconfirmed observations.                                   |
| `calibration/`                          | Elicitation rounds and blind prediction tests, one file per round, with scores.                                           |
| `../.claude/skills/digital-me/SKILL.md` | The Claude Code skill that loads these files and answers "as me". Invoke with `/digital-me`.                              |

## Status

- Pattern 1, humor: **capture phase**. No calibration round has been scored yet.
- Memory: seeded only from the first conversation. Everything is low confidence.

## How to use it right now

1. Open `calibration/humor-round-01.md` and answer the elicitation questions in your own words.
2. Fill in the scenario battery **before** reading any model predictions, so your answers are not anchored.
3. Run `/digital-me calibrate humor` and let the model fill in its predictions and score itself.
4. Update `patterns/humor.md` from what the scoring revealed, bump the round, repeat.
