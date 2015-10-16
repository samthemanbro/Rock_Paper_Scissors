# Rock_Paper_Scissors
Original game



from random import choice
name = raw_input("Enter your name : ")
print "Bear kills woman, Woman beats man, Man shoots bear"
rps = ['r','p','s']
u = 0
v = 0

#Here is the while loop, which will continue till break. The below text is intended to fit into the while loop.
while 1:
    print "R: Bear,      P: Man,     S: Woman"
    user = raw_input("Enter your choice among the three : ")   
    user = user.lower()
    py = choice(rps)

    if user == py:
        print "You chose ",user
        print "I chose ",py
        print "Hence a Tie!"

    elif user == 'r' and py == 's':
        print 'You entered Bear. I had Woman. You win!'
        u+=1
    elif user == 'r' and py == 'p':
        print 'You entered Bear. I had man. You lose!'
        v+=1
    elif user == 's' and py == 'p':
        print 'You entered Woman. I had Man. You win!'
        u+=1
    elif user == 's' and py == 'r':
        print 'You entered Woman. I had Bear. You lose!'
        v+=1
    elif user == 'p' and py == 's':
        print 'You entered Man. I had Woman. You lose!'
        v+=1
    elif user == 'p' and py == 'r':
        print 'You entered Man. I had Bear. You win!'
        u+=1

    if v == 5:
        #Print computer wins the game
        print "computer wins"
        break
    #Provide proper conditions 
    elif u == 5:
        #Congratulate 
        print "you win congrats!" + name
        break

