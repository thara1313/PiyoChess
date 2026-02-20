# PiyoChess

PiyoChess is a cute mini-chess puzzle game built with Flutter.  
Players progress through 45 unique puzzle stages, unlock stories,  
and enjoy original character designs.

## Features
- 5x7 mini–chess battle system  
- AI battle mode (enemy logic built with evaluation + search)  
- 45 puzzle courses with increasing difficulty  
- Story mode & character gallery  
- Offline play  
- Cute animations, sound effects, and UI  
- Works on iOS & Android

## Gameplay Interaction Proposal
- Allow players to tap enemy pieces directly when those pieces are in a legal capture state.
- If a tap is valid, execute a capture animation and remove the enemy piece from the board.
- Set the stage clear condition to: **tap-capture the enemy King**.
- Show a short feedback flow after King capture:
  - "Checkmate!" banner
  - clear animation / SFX
  - stage clear dialog (`Next`, `Retry`, `Back to Map`)

### Recommended Tap Flow
1. Tap one of your pieces to show legal move/capture targets.
2. Tap a highlighted enemy piece to capture.
3. If the captured piece is the King, trigger clear immediately.

### Safety / UX Notes
- Ignore taps on non-highlighted enemy pieces (no accidental invalid actions).
- Add optional haptic or sound feedback for valid taps to improve responsiveness.
- Keep a small `Undo` or `Reset` option for puzzle users who mis-tap.

## Tech Stack
- Flutter 3.x
- Provider (state management)
- just_audio (BGM & SFX)
- Custom game engine (board logic, movement, enemy AI)
- Local storage (progress save)
- Responsive UI, custom painting, tween animations

## Folder Structure
