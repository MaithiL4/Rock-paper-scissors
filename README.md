# Rock-paper-scissors
Rock paper scissors.  is an intransitive hand game, usually played between two people, in which each player simultaneously forms one of three shapes with an outstretched hand. These shapes are "rock" (a closed fist), "paper" (a flat hand), and "scissors".The earliest form of "rock paper scissors"-style game originated in China and was subsequently imported into Japan, where it reached its modern standardized form, before being spread throughout the world in the early 20th century.
#we are going to use Random Module in python. Python has a built-in module that you can use to make random numbers.

#code start here

import random

def play():
    user = input("whats your choice? 'r' for rock, 'p'for paper, 's' for scissors\n ")
    computer = random.choice(['r', 'p', 's'])
    
    if user == computer:
        return 'it\'s a tie'
    
    if is_win(user, computer):
        return 'you won!'
    return 'you lost!'

    
def is_win(player, opponent):
    #retun true if player wins
    # r>s, s>p, p>r
    if (player == 'r' and opponent == 's') or (player == 's' and opponent == 'p')\
        or (player == 'p' and opponent == 'r'):
        return True

print(play())
