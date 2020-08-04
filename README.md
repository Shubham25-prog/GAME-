# GAME
#SNAKE - WATER -GUN

import random
lst = ["S", "W", "G"]
#chance= 10
computer_point = 0
human_point = 0
draw_point = 0
i=0
for i in range(1,11):
        #lst = ["S", "W", "G"]
        computer= random.choice(lst)
        human= input("Choose any one S:(Snake),W:(Water),G:(Gun) :")
        if computer=="S":
            if human=="G":
                human_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"you win this round \n")
                print(f"number of remaining chance is :",10-i)
            elif human=="W":
                computer_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"computer win this round \n")
                print(f"number of remaining chance is :", 10-i)

            else:
                draw_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"round draw \n")
                print(f"number of remaining chance is :", 10-i)


        if computer=="W":
            if human=="S":
                human_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"you win this round \n")
                print(f"number of remaining chance is :", 10 - i)

            elif human=="G":
                computer_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"computer win this round \n")
                print(f"number of remaining chance is :", 10-i)

            else:
                draw_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f" round draw \n")
                print(f"number of remaining chance is :", 10-i)

        if computer=="G":
            if human=="S":
                computer_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"computer win this round \n")
                print(f"number of remaining chance is :", 10-i)

            elif human=="W":
                human_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"you win this round \n")
                print(f"number of remaining chance is :", 10-i)

            else:
                draw_point+=1

                print(f"your guess is {human} and computer guess is {computer} \n")
                print(f"round draw \n")
                print(f"number of remaining chance is :", 10-i)



print(f'computer wins:{computer_point} you win:{human_point} draw:{draw_point}')
print(f"")
if computer_point>human_point:
    print(f"!!!Congrats Computer!!! \n")

elif computer_point==human_point:
    print(f"!!!Game Draw!!!")

else:
    print(f"!!!Congrats human!!! \n")
