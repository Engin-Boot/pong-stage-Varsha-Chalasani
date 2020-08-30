# update-paddle-status

## Feature

Resets the paddle's position and y-coordinate
as indicated by the players actions.

## Acceptance Criteria

### Scenario: Player slides paddle screen

Given a working interface
And paddle pressed position
And paddle direction

When player slides paddle

Then updates paddle position continously

### Scenario: Player releases paddle

Given a working interface

When paddle released

Then exit update-paddle-status module