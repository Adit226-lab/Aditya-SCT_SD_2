// Aditya-SCT_SD_2

//this is a number guessing game
#include <iostream>
#include <cstdlib>  
#include <ctime>
using namespace std;


int main(){


int number;
int guess;
int tries = 0;
int maxTries = 5;

srand(time(NULL));
number = (rand()%100)+1;


cout<<"***** WELCOME TO THE NUMBER GUESSING GAME *****\n";



do{
cout<<"guess a number between 1 - 100:\n";
cin>>guess;
tries++;

if(guess>number){
    cout<<"Too high! Try again.\n";
} else if(guess<number){
    cout<<"Too low! Try again.\n";
} else {
    cout<<"Congratulations! You've guessed the number "<<number<<" in "<<tries<<" tries.\n";
}

if(tries >= maxTries && guess != number) {
    cout<<"Sorry, you've used all your tries. The number was "<<number<<". Better luck next time!\n";
    break;}

}while(guess!=number);

return 0;
}

