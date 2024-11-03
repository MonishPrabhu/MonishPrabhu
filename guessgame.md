import random

def guessing_game():
    number_to_guess = random.randint(100, 1000)
    attempts = 15  # Number of chances

    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 100 and 1000.")
    print(f"You have {attempts} chances to guess the number.")

    for attempt in range(attempts):
        try:
            guess = int(input(f"Attempt {attempt + 1}: Make a guess: "))
            num = r.randint(100, 1000)
            if num<100:
                num+=100
                num1=str(num)
                count=1
                while (count !=11):
                    num2=input(f"enter guess {count}:")
                if int(num2)<100 or int(num2)>=1000:
                    print("invalid input")
                    continue
                count+=1
                if num1==num2:
                    for j in range(len(num2)):
                        flag=0
                        if (num1[j]== num2[j]):
                            print("fermi",end=" ")
                            flag=1
                        if (num2[j] in num1 and flag==0):
                            print("pico",end=" ")
                            print("\n")
                        else:
                            break
                    print(f"\nYou failed. Number is {num}" if attempts>=15 else f"\nYou got it!! Guess was {num}")



