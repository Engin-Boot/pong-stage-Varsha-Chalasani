# update-score-card

## Feature

It checks the collision status and updates
the score card of players accordingly.

## Acceptance Criteria

### Scenario: Player one's paddle collides with ball

Given a working interface
And player one current score

When collision is detected

Then update player one's score and return

### Scenario: Player two's paddle collides with ball

Given a working interface
And player two current score

When collision is detected

Then update player two's score and return

### Scenario: Ball collides with player boundary

Given a working interface
And current player name
And players' current score

When ball collides with boundary

Then return current scores
