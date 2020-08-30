# update-score-card

## Feature

It checks the collision status and updates
the score card of players accordingly.

## Acceptance Criteria

### Scenario: Ball misses collision

Given a working interface
And current player name
And players' current counters

When ball misses collision with paddle

Then increment no-Collision-Count
And check condition

### Scenario: Ball misses collision for more than thrice

Given a working interface
And current player name
And players' current counters

When one player's no-Collision-Count
greater than 3

Then increment no-Collision-Count
And move to declare-winner module
