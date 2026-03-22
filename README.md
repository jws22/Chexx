# Chexx: Hex Chess Variant – 51-cell Board

**Chexx** is a two-player chess-inspired strategy game played on a 51-hex board. This is the current official ruleset and board configuration on `main`.  
_An alternate (classic 91-cell) version is preserved in the `Full6-Board` branch._

---

## Board

- The board is a **rectangular hexagonal array**: 7 rows, in widths 6-7-8-9-8-7-6 (total: 51 hexes).
- Player 1 begins at the bottom, Player 2 at the top.

---

## Setup

**13 pieces** for each player, arranged in 2 rows on their edge.

- **Front row** (7 hexes, closest to opponent):  
  `Knight – Shield – Shield – Shield – Shield – Shield – Knight`
- **Back row** (6 hexes, left to right):  
  `Knight  ·  Ballista  ·  King  ·  Queen  ·  Ballista  ·  Knight`

---

## Pieces and Movement

**Shield** (acts like a pawn)
- Moves **one hex forward only**, either straight or forward-diagonal.
- **Cannot move backward.**
- **Capture:** Any non-Shield enemy doubly-covered by two of your Shields is automatically removed. Shields do not capture by moving.

**Ballista** (artillery)
- May **move one hex in any direction** (like a king) or **fire** as its turn action.
- **Fires** in a straight line along any of the six hex axes; destroys the first enemy piece in its line of sight (cannot shoot through friends).
- **Shields** are _immune_ to Ballista fire from their "front" – attacks must come from the flanks or rear.
- Cannot move and fire in one turn.

**Knight**
- Moves via a "hex knight's move": two hexes in any direction, with a mandatory 60° turn after the first hex; jump ignores intervening pieces.
- **Captures** any enemy on the landing hex.
- May also **retreat** one hex directly backward (away from the enemy's edge). This is a non-capturing move.

**Queen**
- Moves any number of hexes along any single axis (six directions), blocked by pieces in its path.
- **Capture:** Moves onto an enemy's hex.
- **Shield Immunity:** If a Queen attacks a Shield from the Shield's front, the Queen stops before the Shield instead of capturing.

**King**
- Moves and captures one hex in any direction.
- Cannot move into check (threatened hex).
- Is not blocked by the Shield's front-facing immunity.

---

## Special Rules

- **Check & Checkmate:** Played as in chess – you must escape check, and a King in checkmate loses instantly.
- **No promotion:** Shields never promote, even on reaching the far side.
- **Game ends if a King is checkmated.**

---

## Project Structure

- `index.html` – Main 51-cell board implementation
- `Full6-Board` branch – Classic 91-cell "large hex" version and legacy README

---

## Alternate Versions

- The **original 91-cell version** is archived in the [`Full6-Board` branch](https://github.com/jws22/Chexx/tree/Full6-Board). See that branch for setup, rules, and historical info about the classic version.

---

## Credits

- Game rules, board design, and implementation: [jws22](https://github.com/jws22)

---