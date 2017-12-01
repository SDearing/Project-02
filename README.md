# Project-02
Second project of Video Games Design HND course at West Herts College
## Project Outline ##
A player is shown a random playing card, then asked to decide whether the next card will be ‘higher’ or ‘lower’. If the guess is correct the player is awarded with a ‘cash’ prize.
## Functional Specifications ##
*	The program will need to display cards to the user
*	The program will need to pick a card randomly to display
*	The program will need to allow the user to input their guess of whether the next card will be higher or lower
*	The program will need to only allow the user to input the strings “higher” or “lower” to reduce chances of error
*	The program will need to be able to determine the value of playing cards
*	The program will need to be able to compare the value of playing cards, to see if they are higher or lower than the original
*	The program will need to be able to determine whether the user’s guess was correct or incorrect
*	The program will need to be able to award the user a cash prize if they are correct
*	The program will need to be able to store the amount of cash the user has generated and allow that cash variable to be increased when the user correctly guesses
*	The program will need to be on a loop so the user can play multiple rounds of the game
*	The program will need to allow the user to exit the game whenever they please
## Non- Functional Specifications ##
*	The program will need to display to the user what the first card is, by showing a written description of the cards attributes.
*	The program will need to display to the user a written description of what the new card is after they have inputted their guess
*	The program will need to clearly display when it is time for the user to input their guess
*	The program will need to display to the user what their cash score is and show when that value is increased
*	The program will need to display to the user when they have guessed correctly or incorrectly
*	The program will need to display to the user when a new round has started 
## Overall Look ##
The game will be text based, it will display cards by generating a description of the card, a number between 1-13 will be generated, if the number is 1 it will be transferred to an Ace, if the number is 11 it will be transferred to a Jack, if 12 is generated it will be transferred to a queen and if a 13 is generated it will be transferred to a king. Then a suit will be generated from the selection of ‘Hearts’, ‘Clubs’, ‘Spades’ and ‘diamonds’.  This will then be displayed to the user by printing a phrase structured like so: “Your card is ‘number’ of ‘suit’. <br />
The program will tell the user when an input is required, this input will always be the user typing in either “higher” or “lower. If the user guesses correctly they will be awarded £10 however if they guess incorrectly they will lose £10, the game will end once the user has scored £100
## User Story ##
