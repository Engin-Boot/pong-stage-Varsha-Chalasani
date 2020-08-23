# Interaction Sequences

## Startup Sequence

sequenceDiagram
  create-new-game->>+create-new-game: set background UI
  create-new-game->>+create-new-game: set initial ball position and direction
  create-new-game->>+create-new-game: set paddles' positions
  create-new-game->>+take-player-name: update UI
  take-player-name->>+create-new-game: stores player's name
  create-new-game->>+launch-game: click 'start'
  launch-game->>+launch-game: 3 second timer

## Movement Initiation

sequenceDiagram
  launch-game->>+set-paddle-position: random() direction
  set-paddle-position->>+check-collision: moves paddle
  check-collision->>+set-ball-direction: computes the new direction
  check-collision->>+declare-winner: collision with boundary
  set-ball-direction->>+set-paddle-position: change ball direction

## One score

sequenceDiagram
  set-ball-direction->>+check-collision: change ball direction
  check-collision->>+update-score-card: detect current player
  update-score-card->>+set-ball-direction: increment score
  check-collision->>+declare-winner: end game
  declare-winner->>+update-score-card: request scores
  update-score-card->>+declare-winner: send scores
  declare-winner->>+declare-winner: display scores
