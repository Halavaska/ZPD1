## izveidot number guessing spēli izmantojot python

### saturs

#### aprakstīt spēli 
interesanta spēle kas atista loģiku
#### spēles loģistika
dators ģenerē 1-100 ciparu
spēles loģistika ir labi aprakstīta šeit
``py

    import random

    number = random.randint(1,100)
    guess = 0
    tries = [] 

    while  guess!= number:
    if guess < number:
      print ("pamēģini lielāku")
    else:
      print("pamēģini zemāk")

    guess = int(input("uzmini skaitli :"))
    tries.append(guess)
    else:
      print(f"you win from {len(tries)} tries!")
      print("here is your guessing history")
      print(tries)

    sum_of_differences = 0

    for t in tries:
        sum_of_differences += abs(t - number)

    print(f"average diferance was {sum_of_differences/len(tries)}")
    

