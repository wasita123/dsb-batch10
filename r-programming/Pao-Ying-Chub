## homework - pao ying chub

play_game <- function(rounds = 10) {
  ## play 10 round
  win <- 0
  tie <- 0
  lose <- 0
  for (i in 1:rounds) {
    
    ## define hands
    hands <- c("hammer", "scissors", "paper")
    comp_hands <- sample(hands, 1)
    user_hands <- readline("Choose your hand (hammer, scissors, paper): ")
    
    ## validate input
    if (user_hands == "quit") {
      print("Goodbye!")
      break
    } else if (!user_hands %in% hands) {
      print ("Invalid choice. Please ENTER hammer, scissors, paper.")
    }
    
    ## win/tie/lose
    if (user_hands == comp_hands) {
      result <- "It's a tie !!"
      tie = tie + 1
    } else if ( (user_hands == "hammer" & comp_hands == "scissors") |
                (user_hands == "scissors" & comp_hands == "paper") |
                (user_hands == "paper" & comp_hands == "hammer") ) {
      result <- "You win :)"
      win = win + 1
    } else {
      result <- "You lose :("
      lose = lose + 1
    }
    
    ## show result
    print(paste0("Computer choose: ",comp_hands))
    print(result)
    flush.console()
  }
  
  ## calculate final score
  final_score <- win - lose
  if (final_score < 0) {
    final_result <- "You lost the game :("
  } else if (final_score == 0) {
    final_result <- "It's a tie!"
  } else {
    final_result <- "You won the game :)"
  }
  
  ## show the final score
  print(paste0("You won ",win," round(s)"))
  print(paste0("You tie ",tie," round(s)"))
  print(paste0("You lose ",lose," round(s)"))
  print("The final is ...")
  print(final_result)
}

play_game(5)
