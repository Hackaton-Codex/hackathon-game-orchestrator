---
name: puzzle-design-reviewer
description: Design, audit, and playtest game puzzles for clear goals, fair clues, unique solutions, accurate feedback, accessible controls, and reliable retry behavior. Use for puzzle mechanics or puzzle-related code review.
---

# Puzzle design reviewer

Help make each puzzle understandable, logically solvable, and consistent with the game state and story. Inspect the existing design and implementation before proposing changes; do not redesign unrelated systems.

## Workflow

1. Identify the puzzle's player-facing goal, required knowledge, available clues, input model, accepted solution, feedback, hint path, retry behavior, and success effects.
2. Choose a representation that fits the mechanic and genre. For manipulative tasks such as ordering, assigning, routing, or changing a system state, make the relevant objects and constraints visible; a diagram, map, machine panel, table, or cards may work better than text and generic dropdowns. A visual panel is not mandatory for every puzzle: language, deduction, or abstract logic challenges may be clearer in another form. Decorative art alone does not communicate puzzle state.
3. Solve the puzzle independently from its implementation. Translate clues into explicit constraints and verify whether the intended solution is unique. For small assignment or ordering puzzles, enumerate plausible alternatives when that exposes ambiguity or validator gaps.
4. Compare every input path with the validator. Confirm correct entries succeed, wrong or incomplete entries fail safely, and feedback matches the player's actual attempt. Check that controls allow only intended states or clearly explain how to correct mistakes.
5. Review clue fairness: required information must be visible in the panel or reachable through clearly signposted optional clues. A hint may reveal progressively more; match the hint's strength to the intended difficulty and avoid hidden prerequisite knowledge.
6. Check retries, reset/undo controls, and hint use against the intended penalty model. Preserve any explicitly specified no-penalty retry or hint behavior.
7. Verify success and failure effects against the game state: evidence, counters, attributes, objectives, and persistence should change only when appropriate and should not duplicate on repeated completion.
8. Review accessibility and comprehension: labels, keyboard/focus behavior, readable units, unambiguous terms, and clear explanation after solving.
9. Report the source/reference, intended solution, checks performed, reproducible issues with priority, and concise recommendations. Do not modify game files unless asked.

## Technical and narrative boundaries

- When a puzzle touches a real-world high-stakes domain, distinguish its game mechanic from authoritative legal, safety, engineering, medical, or environmental guidance.
- Do not claim a puzzle is playtested in a browser when only its code or logic was inspected.
- When existing clues conflict, identify the conflict instead of silently choosing a canon answer.
