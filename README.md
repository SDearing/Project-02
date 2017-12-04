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
### FlowChart Explanation ###
The first procedure of the algorithm is to generate the first card, this means that the card's value and suit will be created for the first card. Once the first card has been generated then the user will be required to input either higher or lower, this is will act as the users guess and will be checked later on in the algorithm, once the algorithm has a desired input the second card will be generated. Next the algorithm checks whether the new card is larger than the first, depending on the answer the algorithm will branch to 1 of 2 decisions which will check what the users guess and determine whether they guessed correctly. If the user has guessed correctly they will be awarded £10 to their score, if they did not guess correctly £10 will be taken away from the user's score. Next the algorithm will be looped from the beggining untill the user has a score of £100. Once the user has a score of £100 then they will have won the game and it will end.
## Development Plan ##
### Programming Language ###
The programming language I am going to use to complete this solution is C++, this is because one of the requirements of this project is that I program it in C++.
### IDE ###
To code this program I will use the IDE (Integrated Development Environment) provided by the website repl.it. This website is helpful as it works as a compiler for a very large range of programming languages. Using this IDE will be helpful as it will provide me with more code insight, this is because the repl IDE knows the keywords of C++, meaning that they will be highlighted so that they will stand out so I can easily understand the structure of my code. Another benefit of using an IDE is that it has debugging tools and a built in compiler, which means I can thoroughly test my code before I upload it, and it helps me identify possible errors within my code.
### Coding Standards ###
* In my coding I will use single line comments on most lines of code stating its purpose in the programv so that anyone reading the code can easily see how the sections of code work.
* My variables in the code will be written in CamelCase and will be named after the purpose the variable will serve.
* I will seperate sections of code so that the code is presented clearly, and so someone can more easily understand the code. 
## Development ##
### First Milestone ###
![FirstMilestone](https://github.com/SDearing/Project-02/blob/master/Assets%20for%20Readme/First%20Milestone.PNG)<br/>
This first iteration of the solution randomly generates the first card that will be used in the game. To do this I use the <cstdlib> library to use random functions such as the rand()% function. I first use this function to create a pointer for my Suits list for the suit of the first card, then I use the function to create the value of the first card. Then I present both the first card’s attributes to the user in a clear way. This part of the development is a milestone because I have been able to implement the random functions which I can now use for the rest of my code. <br/>
Now I need to create a similar piece of code that will create the second card that will be compared to the first card. I also need to make a while loop for when the user inputs “higher” or “lower” so that the user will be stuck in a loop until they enter one of those 2 words. This is to improve the robustness of the code by ensuring that the variable will only be two values.

## Finished Code ##
```cpp
//
#include <iostream> 
#include <cstdlib> //imports random libary
#include <array> 

int main()
{
  using namespace std;
  //Variables
  string Suits[4] = {"Hearts","Diamonds","Clubs","Spades"};//List of Suits
  bool GameEnd = false;//Boolean variable to decide when game has ended
  bool CorrectInput = false;//Boolean variable to decide whether users input is correctly entered
  int score=50;//Users Cash Score
  int CardNumber1;//The value of the first card
  string CardSuit1;//The suit of the first card
  int CardNumber2;
  string CardSuit2;
  int pointer;//Pointer for picking a random suit from the list
  string UserChoice;//Users choice of whether the next card will be higher or lower
  
  //Game Introduction
  cout << "Welcome to the card guessing game\n";
  cout << "You will be given a card and will be asked to guess whether the next card will be higher or lower\n";
  cout << "If you guess correctly you be awarded £10, however if you guess wrong you lose £10\n";
  cout << "You will start at £50, and will win the game once you have made £100\n";
  
  //main game loop
  while (GameEnd == false){
    //Presents Score
    CorrectInput = false;
    cout << "Beginning New Round\n";
    cout << "You have £" << score << ".\n";
    //Creates First Card
    pointer = rand()%4; //picks random number between 0-3
    CardNumber1 = rand()% 14 + 1; //picks random number from 1-13
    CardSuit1 = Suits[pointer];
    cout << "Your card is " << CardNumber1;
    cout << " of " << CardSuit1 << ".\n";
  
    //User Input
    while (CorrectInput == false){//while the user doesnt input 'lower' or 'higher'
      cout << "Will the next card be higher or lower?\n";
      cin >> UserChoice;
      if (UserChoice == "higher"){
        CorrectInput = true;
      }
      else if (UserChoice == "lower"){
        CorrectInput = true;
      }
      else{
        cout << "wrong input please only type 'higher' or 'lower'";
      }
    }
    // Creates Second Card
    pointer = rand()%4;
    CardNumber2 = rand()% 14 + 1;
    CardSuit2 = Suits[pointer];
    cout << "Your second card is " << CardNumber2;
    cout << " of " << CardSuit2 << ".\n";
    
    // User Guess Check
    if (CardNumber1 > CardNumber2){
      if (UserChoice == "higher"){
        cout << "You Answered Incorrectly, you will lose £10 \n";
        score = score - 10;
      }
      else{
        cout << "You answered correctly, you will be awarded £10 \n";
        score = score + 10;
      }
    }
    else if (CardNumber1 < CardNumber2){
      if (UserChoice == "higher"){
        cout << "You answered correctly, you will be awarded £10 \n";
        score = score + 10;
      }
      else{
        cout << "You answred incorrectly, you will lose £10 \n";
        score = score - 10;
      }
    }
    else{
      cout << "No difference between cards, restarting round \n";
    }
    
    //Win Condition
    if (score == 100){
      GameEnd = true;
    }
  }
} 
```
