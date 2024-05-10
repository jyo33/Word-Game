
store_g_1=[]
try_p =6
a = input("Enter your name")
print("Welcome to the Word Game",a)
print("6 attempts")

guessed_word = "Dog"
hint = guessed_word[0] + guessed_word[-1]
for guess in range(try_p):
    while True:
        letter = input('Guess the letter:')

        if len(letter) == 1:
            break
        else:
            print("OOPS! please Guess a letter!")
    if letter in guessed_word:
        print('yes!')
        store_g_1.append(letter)
    else:
        print('no!')
    if guess == 3:
        print()
        clue_request = input('Would you like a clue?')
        if clue_request.lower().startswith('y'):
            print()
            print('CLUE: The first letter and last letter of word is:', hint)
        else:
            print('Youre very confident!')
print()
print('''Now Let's see what have you guessed:''',len(store_g_1),'lettters correctly')
print("Those letters are:", store_g_1)

word_guess = input("Guess the whole word:")
if word_guess.lower() == guessed_word:
    print('Congrats! you are correct')
else:
    print('Sorry! The answer was', guessed_word)
    print()
    input("please press enter to leave program")
