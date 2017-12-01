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
![userstory](https://github.com/SDearing/Project-02/blob/master/Assets%20for%20Readme/User%20Story.PNG)
## FlowChart ##
![FlowChart](https://github.com/SDearing/Project-02/blob/master/Assets%20for%20Readme/Flowchart.PNG)
## Development Plan ##
### Programming Language ###
The programming language I am going to use to complete this solution is C++, this is because one of the requirements of this project is that I program it in C++.
### IDE ###
To code this program I will use the IDE provided by the website repl.it. This website is helpful as it works as a compiler for a very large range of programming languages. Using this IDE will be helpful as it will provide me with more code insight, this is because the repl IDE knows the keywords of C++, meaning that they will be highlighted so that they will stand out so I can easily understand the structure of my code. Another benefit of using an IDE is that it has debugging tools and a built in compiler, which means I can thoroughly test my code before I upload it, and it helps me identify possible errors within my code.
### Coding Standards ###
* In my coding I will use single line comments on most lines of code stating its purpose in the programv so that anyone reading the code can easily see how the sections of code work.
* My variables in the code will be written in CamelCase and will be named after the purpose the variable will serve.
* I will seperate sections of code so that the code is presented clearly, and so someone can more easily understand the code. 
## Development ##
### First Milestone ###
![FirstMilestone](https://github.com/SDearing/Project-02/blob/master/Assets%20for%20Readme/First%20Milestone.PNG)<br/>
This first iteration of the solution randomly generates the first card that will be used in the game. To do this I use the <cstdlib> library to use random functions such as the rand()% function. I first use this function to create a pointer for my Suits list for the suit of the first card, then I use the function to create the value of the first card. Then I present both the first card’s attributes to the user in a clear way. This part of the development is a milestone because I have been able to implement the random functions which I can now use for the rest of my code. <br/>
Now I need to create a similar piece of code that will create the second card that will be compared to the first card. I also need to make a while loop for when the user inputs “higher” or “lower” so that the user will be stuck in a loop until they enter one of those 2 words. This is to improve the robustness of the code by ensuring that the variable will only be two values.
