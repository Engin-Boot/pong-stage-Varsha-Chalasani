# update-score-card

## Feature

It checks the collision status and updates
the score card of players accordingly.

## Acceptance Criteria

### Scenario: Ball collides with player boundary

Given a working interface
And current player name
And players' current score

When one player's no-Collision-Count
greater than 3

Then increment no-Collision-Count
And check condition
