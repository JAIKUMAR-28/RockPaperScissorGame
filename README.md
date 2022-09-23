# RockPaperScissorGame

import random

user_wins = 0
computer_wins = 0

options = ['rock','paper','scissor']

while True :
    user_input = input('Type rock/paper/scissor or q to quit: ').lower()
    if user_input == 'q':
        break

    if user_input not in options :
        continue

    random_number = random.randint(0 , 2)
    #rock= 1 , paper= 2 ,scissor= 3
    computer_choose = options[random_number]
    print('Computer Picked', computer_choose+'.')

    if user_input =='rock' and computer_choose == 'scissor':
        print('You Won!')
        user_wins +=1

    elif user_input == 'paper' and computer_choose == 'rock':
        print('You Won!')
        user_wins += 1

    elif user_input =='scissor' and computer_choose == 'paper':
        print('You Won!')
        user_wins +=1

    else:
        print('You lost!')
        computer_wins += 1

print('You Won', user_wins, 'times.')
print('Computer Won', computer_wins, 'times.')
print('Good Bye!')




