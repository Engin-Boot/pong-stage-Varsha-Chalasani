# Interaction Sequences

## Startup Sequence

  create-new-game->>+create-new-game: set background UI
  create-new-game->>+create-new-game: set initial ball position and direction
  create-new-game->>+create-new-game: set paddles' positions
  create-new-game->>+take-player-name: update UI
  take-player-name->>+create-new-game: stores player's name
  create-new-game->>+launch-game: click 'start'
  launch-game->>+launch-game: 3 second timer

## Movement Initiation

  launch-game->>+set-ball-position: random() direction
  set-ball-position->>+update-paddle-status: moves ball
  update-paddle-status->>+check-collision: moves paddle
  check-collision->>+set-ball-direction:
  (collision occurs, computes the new direction)
  check-collision->>+update-score-card:
  (collision misses, computes the new direction)
  update-score-card->>+set-ball-direction:
  (increments counter, no-collision-count<=3)
  update-score-card->>+declare-winner:
  (increments counter, no-Collision-Count>3)
  set-ball-direction->>+set-ball-position: change ball direction

## One score

  set-ball-direction->>+set-ball-position: change ball direction
  set-ball-position->>+check-collision: moves ball
  check-collision->>+set-ball-direction: if collision occurs
  check-collision->>+update-score-card: if collision does not occur
  update-score-card->>+set-ball-direction:
  increment counter, if no-Collision-Count<4
  update-score-card->>+declare-winner:
  increment counter, if no-Collision-Count>=4
  declare-winner->>+declare-winner: display scores
