
module MyModule::RockPaperScissors {

    use aptos_framework::signer;

    /// Struct representing the player's move.
    struct PlayerMove has store, key, drop {
        move_type: u8,  // 0 = Rock, 1 = Paper, 2 = Scissors
    }

    /// Struct representing the computer's move (always set to Rock).
    struct ComputerMove has store, key,drop {
        move_type: u8,  // 0 = Rock
    }

    /// Function to play the Rock, Paper, Scissors game.
    public fun play_game(player: &signer, player_move_type: u8): bool {
        let player_move = PlayerMove { move_type: player_move_type };
        let computer_move = ComputerMove { move_type: 0 };  // Computer always picks Rock

        // Determine the winner (true = player wins, false = computer wins or tie)
        if (is_player_winner(player_move, computer_move)) {
            return true
        } else {
            return false
        };
        return false
    }

    /// Function to check if the player wins against the computer's move.
    fun is_player_winner(player_move: PlayerMove, computer_move: ComputerMove): bool {
        // Rock (0) beats Scissors (2), Paper (1) beats Rock (0), Scissors (2) beats Paper (1)
        (player_move.move_type == 0 && computer_move.move_type == 2) ||  // Rock beats Scissors
        (player_move.move_type == 1 && computer_move.move_type == 0) ||  // Paper beats Rock
        (player_move.move_type == 2 && computer_move.move_type == 1)     // Scissors beat Paper
    }
}
