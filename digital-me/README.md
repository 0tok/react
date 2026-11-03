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

Round 1 runs through a rating page instead of the Markdown table:

1. Open the Humor Lab artifact: https://claude.ai/artifact/LwqzMrYx7fbNw1tVJ2PeRm
2. For each of the 12 scenarios, score every candidate line 0 to 3 on "is this me", mark the
   ones you would laugh at, and type what you would actually say. Each candidate is secretly
   tagged with one humor mechanism; the tags are hidden on the rating screen so they do not
   bias you, and shown aggregated on the Profile tab.
3. Ratings save to the artifact's database. Run `/digital-me score humor` and the model reads
   them back with the artifact data tool, updates `patterns/humor.md` and `memory.md`, and
   pushes new scenarios into the page's `scenarios` collection for round 2.

`calibration/humor-round-01.md` stays as the paper version of the same round and as the
elicitation questionnaire (Part A), which the page does not cover.
