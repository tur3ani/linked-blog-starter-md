#code #project #python 
# code

``` python
import random

NUM_DIGITS = 3
MAX_GUESSES = 20
def main():
    print('''Bagels, a deductive logic game.
          By Al Sweigart al@inventwithpython.com 
        I am thinking of a {}-digit number with no repeated digits.
        Try to guess what it is. Here are some clues:
            
 When I say: Pico That means: One digit is correct but in the wrong position.
 When I say: Fermi That means: One digit is correct and in the right position.
 When I say: Bagels That means: No digit is correct.
 
 For example, if the secret number was 2481 and your guess was 8430, the
 clues would be Fermi Pico.'''.format(NUM_DIGITS))
    while True:
        secretNum = getSecretNum()
        print('I have thought up a number.')
        print('You have {} guesses to get it.'.format(MAX_GUESSES))
    
        numGuesses = 1
        while numGuesses <= MAX_GUESSES:
            guess = ''
            while len(guess) != NUM_DIGITS or not guess.isalnum():
                print('Guess #{}: '.format(numGuesses))
                guess = input('> ')
        
            clues = getClues(guess,secretNum)
            print(clues)
            numGuesses += 1
        
            if guess.lower() == secretNum:
                break
            if numGuesses > MAX_GUESSES:
                print('You ran out of guesses.')
                print('The answer was {}.'.format(secretNum))
            
            print('Do you want to play again? (yes or no)')
            if not input('> ').lower().startswith('y'):
                break
            print('Thanks for playing!')
        
def getSecretNum():
    numbers = list('0123456789abcdefghijklmnopqrstuvwxyz')
    random.shuffle(numbers)
    
    secretNum = ''
    for i in range(NUM_DIGITS):
        secretNum += str(numbers[i])
    return secretNum

def getClues(guess, secretNum):
    if guess == secretNum:
        return 'You got it!'
    clues = []
    
    for i in range(len(guess)):
        if guess[i].lower() == secretNum[i]:
            clues.append('Fermi')
        elif guess[i].lower() in secretNum:
            clues.append('Pico')
    if len(clues) == 0:
        return 'Bagels'
    else:
        clues.sort()
        
        return ' '.join(clues)
    
if __name__== '__main__':
    main()
```

- the .isalnum() function checks if the variable or input is only decimals numbers or alphabet and will give false if it contains anything else like a special character.
- we get the secret code by have a list of numbers using the list number which convert a string to a list then we shuffle said list and take the first "NUM_DIGITS" of characters.
- we go in a for loop to see how many clues in there before printing the clues.
- we use .lower() to make sure you don't have to go through the hassle of getting something case-wrong without knowing.