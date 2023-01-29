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
The game should continue to run in a loop until the number of lifes are utilised or the player managed to guess the word, which ever comes first. 

If the guessed letter is correct, the game should prompt te player accordingly and display the locations of the guessed letter in the word.

![notify user if the guess was correct](https://user-images.githubusercontent.com/53040471/215343750-bf7f3bf0-0b4a-4e56-94bd-049710842c1e.jpg)


### Create functions to run the checks


check_guess and ask_for_input functions were created to group block of codes.

The check_guess function will take the guessed letter as an argument and check if the letter is in the word. The function will first convert the guesses word to be in lower case.

The ask_for_input function will iteratively check if the guessed letter exist inside a word. It will also perform nested function as the check_guess function is being called internally.

Good job so far! But your code probably doesn't look great. It's hard to tell which lines do what.

Create 2 functions, check_guess and ask_for_input functions which contain the code for those two things.

The check_guess function will take the guessed letter as an argument and check if the letter is in the word.

Step 1: Define a function called check_guess. pass in the guess as a parameter for the function. Write the code for the following steps in the body of this function.

Step 2: Convert the guess into lower case.

Step 3. Move the code that you wrote to check if the guess is in the word into this function block.

The ask_for_input function.

Step 1. Define a function called ask_for_input.

Step 2. Move the code that you wrote in the Iteratively check if the input is a valid guess task into this function block.

Step 3. Outside the while loop, but within this function, call the check_guess function to check if the guess is in the word. Don't forget to pass in the guess as an argument to the method.

Step 4. Outside the function, call the ask_for_input function to test your code.

## 4 - Create the Game class

### Create the class

### Create methods for running the checks

### Define what happens if the letter is in the word

### Define what happens if the letter is NOT in the word

## 5 - Putting it all together

### Code the logic of the game



