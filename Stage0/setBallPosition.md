# set-ball-position

## Feature

This module updates ball's position continuously

## Acceptance Criteria

### Scenario: Ball touches a horizontal boundary

Given a working interface
And direction of ball before it touches the boundary

When the ball touches the boundary

Then reset y-coordinate

### Scenario: Ball touches a vertical boundary

Given a working interface
And direction of ball before it touches the boundary

When the ball touches the boundary

Then reset x-coordinate

### Scenario: Ball touches paddle

Given a working interface

When ball touches paddle

Then reset x-coordinate

### Scenario: Ball in movement

Given a working interface
And direction of ball

When the ball moves

Then increment or decrement coordinates
according to directions.

### Scenario: Ball touches a horizontal boundary

Given a working interface
And direction of ball before it touches the boundary

When the ball touches the boundary

Then reset y-coordinate