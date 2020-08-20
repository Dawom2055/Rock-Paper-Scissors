print("Welcome to ROCK, PAPER, SCISSORS!")
print("What is your name?")
name = input()
print('Welcome ' + name + '! have fun playing TicTac Toe')


import random, sys

#These variables will keep track of wins loses and ties

wins = 0
losses = 0
ties = 0

while True:
    print("%sWins , %sLosses, %sTies" %(wins, losses, ties))
    while True:
        print("Enter your move: (r)ock, p(aper), s(cissors) or q(uit)")
        playerMove = input()
        if playerMove == "q":
            sys.exit()
        if playerMove == "r" or playerMove == "p" or playerMove == "s":
            break #We want to break out of player input loop
        print("Type one of r, p, s , or q")

    #Display wehat player chose
    if playerMove == "r":
        print("ROCK versus...")
    elif playerMove == "p":
        print("PAPER versus...")
    elif playerMove == "s":
        print("SCISSORS versus...")

    #Now this will show what the computer is choose we will use the random function
    randomNumber = random.randint(1, 3)
    if randomNumber == 1:
        computerMove = "r"
        print("ROCK")
    elif randomNumber == 2:
        computerMove == "p"
        print("PAPER")
    elif randomNumber == 3:
        computerMove == "s"
        print("SCISSORS")

    #NOW THIS WILL SHOW THE RESULTS
    if playerMove == computerMove:
        print("It's a tie!")
        ties = ties + 1
    elif playerMove == "r" and computerMove == "p":
        print("COMPUTER WINS! " + name + " LOSES")
        losses = losses + 1
    elif playerMove == "p" and computerMove == "s":
        print("COMPUTER WINS! " + name + " LOSES!!")
        losses = losses + 1    
    elif playerMove == "s" and computerMove == "r":
        print("COMPUTER WINS! " + name + " LOSES")
        losses = losses + 1
    elif playerMove == "r" and computerMove == "s":
        print("COMPUTER LOSES!! " + name + " WINS!!")
        wins = wins + 1
    elif playerMove == "p" and computerMove == "r":
        print("COMPUTER LOSSES! " + name + " WINS")
        wins = wins + 1
    elif playerMove == "s" and computerMove == "p":
        print("COMPUTER LOOSES " + name + " WINS!!")
        wins = wins + 1    
   
   



