# set-ball-direction

## Feature

Changes the ball's direction based
on the conditions met.

## Acceptance Criteria

### Scenario: Ball touches paddle of a player

Given a working interface
And direction of ball before it touches the paddle

When the ball touches the paddle

Then ball's direction is reset

### Scenario: Ball touches the other two boundaries

Given a working interface
And direction of ball before it touches the
boundary

When ball touches boundary

Then reset the ball in appropriate direction

### Scenario: Ball touches player boundary and not paddle

Given a working interface

When ball touches player boundary

Then end the game
