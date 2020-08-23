# check-collision

## Feature

Checks the status of collision of ball and player's
paddle and performs an appropriate action.

## Acceptance Criteria

### Scenario: Ball collided with paddle

Given a working interface
And scores of players
And current player name

When ball collided with paddle

Then increment score of relevant player

### Scenario: Ball does'nt collide with paddle

Given a working interface
And current player name

When ball collides with player boundary

Then end game
