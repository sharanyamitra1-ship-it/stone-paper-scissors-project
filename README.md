# stone-paper-scissors-project
import random as r
points=int(input("enter how many points game you want"))
scoreuser=0
scorebot=0
for i in range(points):
    response=input("enter a choice in lower case rock/paper/scissors")
    a=r.randint(0,2)
    if a==1:
        a="rock"
        print("bot chooses",a)
    elif a==2:
        a="paper"
        print("bot chooses",a)
    else:
        a="scissors"
        print("bot chooses",a)
    if a=="rock" and response=="paper":
        scoreuser+=1
    if a=="rock" and response=="scissors":
        scorebot+=1
    if a=="paper" and response=="scissors":
        scoreuser+=1
    if a=="paper" and response=="rock":
        scorebot+=1
    if a=="scissors" and response=="paper":
        scorebot+=1
    if a=="scissors" and response=="rock":
        scoreuser+=1
    if scoreuser==points or scorebot==points:
        break
if scoreuser>scorebot:
    print("userwon,score=",scoreuser)
    print("scoreuser=",scoreuser,"scorebot=",scorebot)
if scorebot>scoreuser:
    print("bot won,score=",scorebot)
    print("scoreuser=",scoreuser,"scorebot=",scorebot)
