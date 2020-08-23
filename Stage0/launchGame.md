# launch-game

## Feature

Loads the game preset interface and
launches the game after a 3 seconds timer.

## Acceptance Criteria

### Scenario: Starting the game after storing
the player details

Given a working interface
And player names set

When on clicking 'Start Game' button

Then start the game after a 3 seconds
timer lapses.

### Scenario: Ball movement after the timer
lapses

Given a working interface
And the initial 3 second timer has lapsed

When the 4th second starts

Then ball moves in a randomly generated
direction

### Scenario: Recovering a paused game

Given a working interface
And the game's condition stored before
pressing pause

When play button is pressed

Then restore the game's conditions
before pausing
