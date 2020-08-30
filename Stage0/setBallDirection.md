# set-ball-direction

## Feature

Changes the ball's direction based
on the conditions met.

## Acceptance Criteria

### Scenario: Ball touches paddle of a player

Given a working interface
And direction of ball before it touches the paddle

When the ball touches the paddle

Then reset ball's direction

### Scenario: Ball touches the horizontal boundaries

Given a working interface
And direction of ball before it touches the
boundary

When ball touches horizontal boundary

Then reset the ball in appropriate direction

### Scenario: Ball misses collision and no-Collision-Count less than 4

Given a working interface

When ball touches vertical boundary

Then reset ball's direction
