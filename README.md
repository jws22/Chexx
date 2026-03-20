# Hex Strategy Game

A two-player strategy game played on a hexagonal board. If you know chess, you'll be at home here.

---

## The Board

The board is a large hexagon made up of 91 smaller hexagons arranged in a honeycomb pattern — six hexes along each side. Each hex has six neighbours. Player 1 sets up along the bottom edge; Player 2 along the top edge. The board is oriented so that "forward" for each player means advancing toward the opponent's edge.

---

## Setup

Each player begins with **13 pieces** arranged across two rows on their edge of the board.

**Front row** (7 hexes, closest to opponent) — 7 Shields

**Back row** (6 hexes, furthest from opponent) — left to right:
Ballista · Knight · King · Queen · Knight · Ballista

---

## Taking Turns

Players alternate turns. On your turn you must either **move a piece** or **fire a Ballista**. If no legal action is available, your turn passes automatically.

---

## The Pieces

### ♟ Shield (chevron icon)
The pawn of this game. Moves one hex forward only — either straight ahead or diagonally forward (the two hexes closest to the opponent's edge). Cannot move backward.

**Capture:** Shields do not capture individually. Instead, any opponent piece (except another Shield) that occupies a hex reachable by **two of your Shields simultaneously** is instantly removed from the board — no move required. This capture is automatic and continuous: it triggers whenever the condition is met, including after the opponent moves.

### ● Ballista (six-pointed star icon)
A stationary artillery piece. On its turn, the Ballista **fires** along any of the six hex axes, removing the first opponent piece in its line of sight. The Ballista itself does not move when firing, though it can also move like a King (one hex in any direction) instead of firing.

Line of fire is blocked by any intervening piece — friendly or opponent. **Exception:** a Shield approached from either of the two directions it naturally moves toward is immune to Ballista fire from those directions. Attack from any other direction and the Shield is a normal target.

### ♞ Knight
Moves like a chess knight adapted for hex geometry: two hexes in any direction, with a mandatory 60° turn after the first hex. The full two-hex jump must be completed — the Knight cannot stop after one hex. The jump ignores any pieces on the path.

The Knight captures any opponent piece — including Shields — on its landing hex.

**Retreat:** The Knight may also move one hex directly backward (away from the opponent's edge) as an alternative to its jump. This is a non-capturing move only, and retreat hexes are not considered threatened for the purposes of King safety.

### ♛ Queen
Slides any number of hexes along any of the six axes, exactly like a chess queen but with six directions instead of eight. Blocked by any piece in its path. Captures by moving onto an opponent's hex.

**Exception:** a Shield approached from either of its own forward directions is immune — the Queen's slide stops at the hex before it without capturing.

### ♚ King
Moves and captures one hex in any direction — identical to the chess King. Cannot move into a hex threatened by any opponent piece.

The King can capture a Shield from any direction (the Shield's directional immunity does not apply to the King).

---

## Check & Checkmate

These work exactly as in chess.

- **Check:** your King occupies a hex threatened by an opponent piece. When in check you must resolve it on your turn — you cannot make an unrelated move.
- **Resolving check:** move the King to safety, interpose a piece to block the threat, or capture the threatening piece with any piece.
- **Checkmate:** the King is in check and no legal move resolves it. The game ends immediately and the opponent wins.

### What counts as a threat?
A hex is threatened if any opponent piece could legally move or attack there:
- A **Knight** threatens all its possible landing hexes (not its retreat hexes)
- A **Queen** or **Ballista** threatens all hexes in their line of fire (respecting the Shield immunity rule)
- A **King** threatens all six adjacent hexes
- A pair of **Shields** that doubly-cover a hex count as a threat to the King (matching the capture rule)

---

## Quick Reference

| Piece | Move | Captures |
|---|---|---|
| Shield | 1 hex forward | Automatic — any non-Shield piece doubly-covered by 2 Shields |
| Ballista | 1 hex any direction, or fire along any axis | First piece in line of fire (stationary when firing) |
| Knight | 2-hex jump with 60° turn; or 1 hex retreat | Any piece on landing hex |
| Queen | Unlimited slide along any axis | Any piece on destination hex |
| King | 1 hex any direction | Any piece on destination hex (cannot move into check) |

---

## Key Differences from Chess

- **Six directions** instead of four/eight — every piece has more routes to consider.
- **No promotion** — Shields remain Shields for the whole game.
- **Ballista fires in place** — a long-range threat that never needs to advance.
- **Shield wall** — two Shields working together passively eliminate any piece that walks between them, creating a powerful advancing front.
- **Directional Shield immunity** — Shields have a protected facing. Queens and Ballistae must flank to break through a Shield line.
- **Knight retreat** — Knights can step backward one hex, giving them a tactical escape not available in chess.
