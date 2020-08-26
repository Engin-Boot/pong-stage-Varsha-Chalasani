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

  launch-game->>+set-paddle-position: random() direction
  set-paddle-position->>+check-collision: moves paddle
  check-collision->>+set-ball-direction: computes the new direction
  check-collision->>+set-ball-direction: computes the new direction
  (if collision occurs snd no-Collision-Count<4)
  check-collision->>+declare-winner: collision with boundary
  (if collision occurs and no-Collision-Count>=4)
  set-ball-direction->>+set-paddle-position: change ball direction

## One score

  set-ball-direction->>+check-collision: change ball direction
  check-collision->>+set-ball-direction: if collision occurs
  check-collision->>+update-score-card:
  if collision does not occur increment no-Collision-Count
  update-score-card->>+set-ball-direction: if no-Collision-Count<4
  update-score-card->>+declare-winner: if no-Collision-Count>=4
  declare-winner->>+declare-winner: display scores
