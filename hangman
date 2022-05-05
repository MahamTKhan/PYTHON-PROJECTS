import random
import time

words=["apple","maham","pakistan","juice","banana","hello","software","games","engineering","mathematics","english","urdu"]


def select_word():
    selected_word=random.choice(words)
    return selected_word.upper()

def hangman(turns):
    attempts=["""
               -------
               |      |
               |      0
               |     \|/
               |      |
               |     / /
               |
               -
               """,
               """
               -------
               |      |
               |      0
               |     \|/
               |      |
               |     / 
               |
               -                        
               """,
               """
               -------
               |      |
               |      0
               |     \|/
               |      |
               |     
               |
               -                        
               """,
               """
               -------
               |      |
               |      0
               |     \|/
               |      
               |      
               |
                -                        
                """,
                """
                -------
                |      |
                |      0
                |     \|
                |      
                |      
                |
                -                        
                """,
                """
                -------
                |      |
                |      0
                |     /
                |      
                |      
                |
                -                        
                """,
                """
                -------
                |      |
                |      0
                |     
                |      
                |      
                |
                -                        
                """,
                """
                -------
                |      |
                |      
                |     
                |      
                |      
                |
                -                        
                """,
    ]
    return attempts[turns]

def hangman_game(word):
    name=input("enter your name:")
    print("best of luck",name)

    points=0
    turns=7
    guessed=False
    your_guesses=[]
    print(hangman(turns))
    length_of_word=len(word)
    guess_the_word="_"*length_of_word
    print(guess_the_word)

    while not guessed and turns>0:
        guess=input("guess a letter:").upper()
        if len(guess)==1 and guess.isalpha():
            if guess in your_guesses:
                print("you have already guessed",guess)
            elif guess not in word:
                print(guess,"is not in the word")
                turns-=1
                your_guesses.append(guess)
            else:
                print(guess,"is in the word")
                your_guesses.append(guess)
                chars_of_word=list(guess_the_word)
                indices=[i for i,letter in enumerate(word) if letter==guess ]
                for index in indices:
                    chars_of_word[index]=guess
                    guess_the_word="".join(chars_of_word)
                    if "_" not in guess_the_word:
                        guessed=True
                        guess_the_word=word

                if guessed :
                    print("CONGRATULATIONS", name, "YOU WON :)")
                else:
                    print("YOU LOST! :( BETTER LUCK NEXT TIME")


            print(hangman(turns))
            print(guess_the_word)
            print(your_guesses)


def start_game():
    word=select_word().upper()
    hangman_game(word)
    play_again=input("do you want to play again?Y|N").upper()
    if play_again=="Y":
        word = select_word().upper()
        hangman_game(word)
    else:
        time.sleep(5)
        exit()

start_game()
