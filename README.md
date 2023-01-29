# Hangman Project Documentation

## 1 - Setup the environment
Repository was created at GitHub. First commit was completed to verify that the local git folder can be synced with the remote repository.

## 2 - Create the variables for the game

### Define the list of possible words
The list contains the names of 5 fruits. It was then assigned to a variable called word_list.

### Choose a random word from the list
Randam library was imported to enable the random function where the programme should randomly select a word from the word list. random.choice function was tested by continuously printing the result from calling the function and verify that the selection of word is automated as well as random.

### Ask the user for an input
Utilises python input function to prompt user to enter the input

### Check that the input is a single character
The length function is being used to check if the entered input is a single letter.

## 3 - Check if the guessed character is in the word

### Iteratively check if the input is a valid guess
The game should prompt the player that he or she could only enter one letter at a time. In case more than one letters were enterred, the program should alert that the input was invalid.

![asked the user to enter only one letter](https://user-images.githubusercontent.com/53040471/215342083-0ee04777-c824-4af5-864a-e4dbaa2dae27.jpg)
### Check whether the guess is in the word
The game should continue to run in a loop until the number of lives are utilised or the player managed to guess the word, which ever comes first. 

If the guessed letter is correct, the game should prompt te player accordingly and display the locations of the guessed letter in the word.

![notify user if the guess was correct](https://user-images.githubusercontent.com/53040471/215343750-bf7f3bf0-0b4a-4e56-94bd-049710842c1e.jpg)


### Create functions to run the checks

Blocks of related codes were grouped into functions. 

The check_guess function will take the guessed letter as an argument and check if the letter is in the word. The function will first convert the guesses word to be in lower case.

The ask_for_input function will iteratively check if the guessed letter exist inside a word. It will also perform nested function as the check_guess function is being called internally.

## 4 - Create the Game class

### Create the class
Hangman class was created to further structure the codes for the game. The class has the following attributes:

1. word: The word to be guessed, picked randomly from the word_list. The random library was imported at the beginning of the script.
2. word_guessed: list - A list of the letters of the word, with _ for each letter not yet guessed. For example, if the word is 'apple', the word_guessed list would be ['_', '_', '_', '_', '_']. If the player guesses 'a', the list would be ['a', '_', '_', '_', '_'].
3. num_letters: int - The number of UNIQUE letters in the word that have not been guessed yet.

![user cannot continue to enter the same letter](https://user-images.githubusercontent.com/53040471/215347845-addeb5bd-4236-4e7d-a511-bb90d94fac6a.jpg)

4. num_lives: int - The number of lives the player has at the start of the game.
5. word_list: list - A list of words.
6. list_of_guesses: list - A list of the guesses that have already been tried. The list was set to an empty list initially.

![inform the user in case the following guess was wrong n update the lifes left ii](https://user-images.githubusercontent.com/53040471/215347989-0e0f2801-616c-4db9-80aa-f3b53375b1f9.jpg)


### Create methods for running the checks

### Define what happens if the letter is in the word
Should the guessed letter is in the word, the code would display the location of the gussed word.

![program will display all locations of the letter if the letter is in the word](https://user-images.githubusercontent.com/53040471/215347921-e03e8587-a86e-4fb0-a657-79a2975a403e.jpg)

![program will display all locations of the letter if the letter is in the word ii](https://user-images.githubusercontent.com/53040471/215347924-0b5bedbf-b030-4221-b00a-472d8b133f5b.jpg)

### Define what happens if the letter is NOT in the word
Upon an incorrect input, the game would:

1. Reduce `num_lives' by 1.
2. Print a message saying "Sorry, {letter} is not in the word."
3. Print another message saying "You have {num_lives} lives left."

![inform the user in case the following guess was wrong n update the lifes left](https://user-images.githubusercontent.com/53040471/215347992-4d856b90-28d8-4205-99a7-c10708f31449.jpg)

The user is not allowed to enter the same character.

![user cannot continue to enter the same letter](https://user-images.githubusercontent.com/53040471/215355876-994bd7c6-f186-4541-ab6b-c4c35a2d734a.jpg)

If the player exceeded the five wrong attempts, the game would end and declare that the player has just lost the game.

![all attemps were wrong acknowledge that game is over](https://user-images.githubusercontent.com/53040471/215355943-faf0828a-0ff3-4e51-b456-9abb1c272f5a.jpg)

## 5 - Putting it all together

### Code the logic of the game
Rearranged the codes to include the class and functions at the start, then place the call to a function to start the game at the very end. For successful gusses and attempts within the allowable number of lives, the player will be acknowledged as the winner.

![upon correct guess acknowledge the winner ii](https://user-images.githubusercontent.com/53040471/215355804-5cf1687e-e6ec-4ded-a8d9-a548f212f03b.jpg)

![upon correct guess acknowledge the winner](https://user-images.githubusercontent.com/53040471/215355806-d952bdfc-8cb9-41ff-83d5-4be2841ff747.jpg)



