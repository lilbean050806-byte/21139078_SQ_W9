# Week 9 Example 3 — Higher or Lower

## What This Example Demonstrates

This example is a card guessing game across 3 JSON-driven levels. A card is shown face up — guess whether the next card in the shuffled deck is higher or lower. Reach the target score to advance. Guess wrong and it's game over.

- **`sketch.js`** — all game logic
- **`data/level1.json`** — 8 cards, target score 5
- **`data/level2.json`** — 13 cards, target score 8
- **`data/level3.json`** — 26 cards (2 suits), target score 12

## Debug Panel (Side Quest — Complete)

Press **D** at any time, on any screen, to toggle a debug panel in the top-right corner. It shows the live game state and every shortcut, so nothing needs to be memorized while testing:

- **state** — current game state (start / play / win / over)
- **level** — current level out of `MAX_LEVELS`
- **score** — correct guesses this level vs. the target
- **total** — total correct guesses across the whole run
- **deck** — position in the shuffled deck
- **current / next** — the face-up card and the upcoming card

**Keyboard shortcuts**

- **D** — Toggle the debug panel
- **1** — Jump straight into Level 1
- **2** — Jump straight into Level 2
- **3** — Jump straight into Level 3
- **S** — Jump to the start screen
- **W** — Jump to the win screen
- **O** — Jump to the game over screen
- **N** — Force-deal the next card (skip ahead in the deck)

The level shortcuts (**1**/**2**/**3**) call `loadLevel()` directly and drop you into `STATE_PLAY`, so you can test any level's cards and target score without playing through the ones before it. **S**, **W**, and **O** jump straight to their respective screens for quick visual checks. **N** steps through the current deck one card at a time without needing a correct/incorrect guess, which is handy for confirming deck order and end-of-deck behavior.

## Setup and Interaction Instructions

To run the sketch locally, open `index.html` in Google Chrome using Live Server.

Click **Higher ▲** or **Lower ▼** to guess. Reach the target score shown in the HUD to advance to the next level. Equal cards count as wrong — you must commit to a direction.

**Opening the Chrome Console**

- **Windows:** Press `F12` or `Ctrl + Shift + J`, then click the **Console** tab
- **Mac:** Press `Cmd + Option + J`

## Assets

No external assets used. All visuals are generated with p5.js.

## References

N/A