# Verification Strategy

## Critical behaviors

- An editor can correct a transcript before using it in a synthesis.
- Concurrent edits do not silently overwrite one another.
- A generated proposal does not replace an intervening human revision.
- A finalized PDF corresponds to the intended finalized content.

## Test layers

| Layer | Focus |
|---|---|
| Unit | Domain rules, validation and state changes without live external dependencies. |
| Integration | Consistency across application services and their storage or external-service adapters. |
| User journey | A complete path from a user action to its visible outcome, including failure states. |

## Environment checks

Interviews and job profiles contain sensitive HR material. Access control, private file delivery and human review are central to the design.
