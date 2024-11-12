#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed the random number generator
    std::srand(static_cast<unsigned>(std::time(0)));
    int randomNumber = std::rand() % 100 + 1; // Random number between 1 and 100
    int userGuess = 0;

    std::cout << "Welcome to the Guess the Number game!" << std::endl;
    std::cout << "I have chosen a number between 1 and 100." << std::endl;

    // Loop until the user guesses the correct number
    while (userGuess != randomNumber) {
        std::cout << "Enter your guess: ";
        std::cin >> userGuess;

        if (userGuess > randomNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else if (userGuess < randomNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the correct number: " << randomNumber << std::endl;
        }
    }

    return 0;
}
