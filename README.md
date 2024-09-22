# AptosWeb3
Rock Paper Scissor Aptos Web3 

# RockPaperScissors on Aptos Blockchain

## Vision
The **RockPaperScissors** project is a blockchain-based implementation of the classic game "Rock, Paper, Scissors," built on the Aptos blockchain. The vision is to demonstrate the power and simplicity of smart contracts in the Aptos ecosystem by creating a decentralized, transparent, and immutable game. This project serves as an educational example of using Aptos blockchain technology to deploy interactive, on-chain games and smart contracts.

## Features

- **Blockchain-based Game:** The game logic is fully decentralized, with moves and outcomes stored on the Aptos blockchain.
- **Simple Game Logic:** Players choose from Rock, Paper, or Scissors, while the computer always selects Rock. The game determines the winner based on predefined rules.
- **Smart Contract-Driven:** The game is implemented using Aptos Move language, ensuring that all moves and results are verifiable and immutable.
- **Transparent Outcomes:** Since the game logic is public, anyone can verify the outcomes of the game by inspecting the blockchain state.
- **Lightweight Structs:** Both player and computer moves are represented by simple structures for optimized storage and processing.

## Contract Information

### Structs
- **PlayerMove**
  - **Attributes:** 
    - `move_type: u8` – Represents the player's choice (0 = Rock, 1 = Paper, 2 = Scissors).
  - **Abilities:** `store, key, drop`
- **ComputerMove**
  - **Attributes:**
    - `move_type: u8` – Always set to `0` (Rock).
  - **Abilities:** `store, key, drop`

### Functions

- **play_game**
  - **Arguments:** 
    - `player: &signer` – The signer's account.
    - `player_move_type: u8` – The move chosen by the player (0 = Rock, 1 = Paper, 2 = Scissors).
  - **Returns:** 
    - `bool` – Returns `true` if the player wins, otherwise `false`.
  - **Logic:** 
    - Compares the player's move with the computer's move (which is always Rock) and returns the result based on game rules.
  
- **is_player_winner**
  - **Arguments:** 
    - `player_move: PlayerMove` – The player's move.
    - `computer_move: ComputerMove` – The computer's move (always Rock).
  - **Returns:** 
    - `bool` – Returns `true` if the player wins against the computer's move.
  - **Logic:**
    - Follows traditional Rock, Paper, Scissors rules: Rock (0) beats Scissors (2), Paper (1) beats Rock (0), and Scissors (2) beats Paper (1).

## Future Scope

The current implementation of **RockPaperScissors** is a minimalistic demonstration of Aptos smart contract capabilities. Future developments could include:

- **Multiplayer Mode:** Extend the game to allow two players to compete against each other in a decentralized manner, with both moves recorded on-chain.
- **Randomized Computer Moves:** Introduce randomness to the computer's move, enabling it to choose between Rock, Paper, and Scissors rather than always selecting Rock.
- **Token Rewards:** Integrate cryptocurrency rewards, allowing players to earn tokens based on game outcomes.
- **Leaderboards:** Implement on-chain leaderboards to track player performance and showcase top winners.
- **Custom Tournaments:** Create organized tournament structures where players can compete for prizes in a decentralized, transparent manner.
  
## How to Deploy

1. Install the Aptos CLI and set up your account.
2. Compile and publish the smart contract code to the Aptos blockchain.
3. Interact with the deployed contract by invoking the `play_game` function with your desired move (Rock, Paper, or Scissors).
  
This project demonstrates the flexibility of the Aptos Move language and offers a foundation for further exploration into decentralized gaming.

## License
MIT License.
