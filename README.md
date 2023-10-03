# rock-paper-sicssors.

#this is a game .paly and win the game and count the scoure.


import random

user_wins = 0
computer_wins = 0

option = ["R", "P", "S"]
while True:
    user_inputs = input("Type R for Rock,"
                             "P for paper,"
                             "S for scissors,"
                         "and Q for quit : ")
    if user_inputs == "Q":
        quit()
        break


    if user_inputs not in option:
        continue

    random_number = random.randint(0,2)

    computer_picks = option[random_number]
    print("computer picked ", computer_picks + ".")

    if user_inputs == "R" and  computer_picks == "S":
        print("you won!!")
        user_wins += 1
    elif user_inputs == "P" and computer_picks == "R":
        print("you won!!")
        user_wins += 1
    elif user_inputs == "S" and computer_picks == "P":
        print("you won!!")
        user_wins += 1
    else:
        print("you lost!!!")
        computer_wins += 1

        print("you won ", user_wins, "times.")
    print("the computer wons ", computer_wins,"times.")
print("goodbye!")
