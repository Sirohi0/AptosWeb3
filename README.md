# AptosWeb3
Rock Paper Scissor Aptos Web3 

# Rock, Paper, Scissors Game on Aptos (Move)

This project implements a simple **Rock, Paper, Scissors** game on the Aptos blockchain using the Move programming language.

## Game Rules

- Rock (0) beats Scissors (2)
- Paper (1) beats Rock (0)
- Scissors (2) beat Paper (1)

The computer always selects Rock as its move, and the player can choose Rock, Paper, or Scissors.

## Functions

### `play_game(player: &signer, player_move_type: u8): bool`
This function allows the player to play a game of Rock, Paper, Scissors. The result (`true` or `false`) is returned depending on whether the player wins or not.

### `is_player_winner(player_move: PlayerMove, computer_move: ComputerMove): bool`
This function checks if the player wins against the computer's move based on standard game rules.

## Project Structure

