#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int guessed,no_of_tries=0;
    // Seed the random number generator with the current time
    srand(time(0));
    // Generate a random number between 1 and 100
    int randomNumber = (rand() % 100) + 1; //A random number between 1 to 100 is stored in the variable randomNumber 
    printf("\n Guess the number\n");
    do
    {
       scanf("%d",&guessed);
       no_of_tries++;
       if(guessed>randomNumber)
       {
        if(guessed-10>randomNumber)
        printf("Oops, you guessed it too high a guess lower\n");
        else
        printf("You guessed a little too high, Nice try though!!!\n");
       }
       else
       {
        if(guessed<randomNumber-10)
        printf("Oops, you guessed it too low a guess high\n");
        else
        printf("You guessed a little too low, Nice try though!!!\n");
       }
    } while(guessed!=randomNumber);
    printf("Congratulations you guessed the number in %d tries \n",no_of_tries);
    return 0;
}
