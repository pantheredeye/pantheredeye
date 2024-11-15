# Synchronized Othello Board

This project aims to create two wall-mounted Othello boards that mirror each other in real-time. Each tile on the board is designed to flip between two colors (black and white) with the following key features:

1. **Push-Flip Tiles**: The tiles can be physically pressed and flipped by the player, providing a satisfying tactile feel for placing their piece.
2. **Automatic Flipping**: The tiles also have a mechanism to automatically flip when necessary, such as flipping the opponent's tiles during gameplay.
3. **Synchronization**: Both boards remain synchronized, meaning automatic flips on one board are replicated on the other, ensuring consistent game states across locations.

## Key Components and Considerations

### Push-Flip Tiles
- Tiles that can be physically pressed and flipped by the player.
- A mechanism behind each tile for automated flipping when needed.

### Dual Flipping Mechanism
- Each tile should be able to flip manually and via a motorized or solenoid actuator.

### Sensing Mechanism
- Detect when a tile is manually flipped by the player.

### Control System
- Microcontrollers to handle input (manual flips), output (automated flips), and synchronization through a network.

### Network Synchronization
- Real-time communication between the two boards to mirror moves and tile flips.

### Indicators & Turn Management
- Visual indicators (LED lights) to show whose turn it is and the game's status.

## Refined Logic Flow

1. **Player's Move with Push-Flip**: The player presses a tile to flip it manually on their board. The microcontroller detects this manual flip.
2. **Game Logic Update**: The controller validates the move and determines which tiles to flip based on Othello rules. Tiles that need to flip automatically do so through motorized actuation.
3. **Automatic Flips & Synchronization**: Simultaneously, the appropriate tiles flip automatically on both the local and remote boards.
4. **Turn Indicator Update**: The system updates LED indicators or other displays to show the next player's turn.
5. **Continuous Play**: Steps repeat until the game concludes.
6. **Game End & Reset**: Once the game finishes, tiles can be returned to the start configuration via an automated reset or manual repositioning.

## Detailed Mechanical & Electronic Explanation

1. **Designing Push-Flip Tiles**: Each tile pivots on an axis or hinge, allowing it to flip 180°. The tile has a manual flip mechanism (like a "rocker switch") and an automatic flip mechanism (servo motor or solenoid).
2. **Sensing Manual Flips**: Micro switches, reed switches, magnetic, or optical sensors detect when a tile is manually flipped by the player.
3. **Implementing the Control System**: Microcontrollers (Arduino, Raspberry Pi) process manual and automatic flipping actions, controlling the actuators and updating the game state.
4. **Networking and Synchronization**: Wi-Fi or Ethernet connects the boards, allowing them to mirror moves and tile states in real-time.
5. **Indicators & Turn Management**: LED lights or a small screen indicate the active player's turn and provide feedback on valid/invalid moves.
6. **Mechanics and Electronics Integration**: Careful mounting of components, power supply management, and a robust enclosure to house the system.
7. **Example Steps with Push-Flip Tiles**: Detailed walkthrough of a manual flip triggering updates and automatic synchronization between the two boards.
8. **Safety and Reliability**: Use durable components, proper power management, and easy access for maintenance.

## Summary

This project combines push-to-flip tile mechanics, automated flipping, and real-time synchronization to create a unique and engaging remote Othello experience. The key features are the tactile feel of manual flips, the automated flipping of captured tiles, and the ability to play against a remote opponent with identical board states.
