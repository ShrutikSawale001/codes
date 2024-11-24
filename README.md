# codes
#include <iostream>
#include <ctime>
#include <cstdlib>

using namespace std;

int main() {
    // Seed for random number generation
    srand(time(0)); 

    int choice;
    char again = 'y';

    // Loop to allow the user to toss the coin multiple times
    while (again == 'y' || again == 'Y') {
        cout << "Enter 1 for Heads or 2 for Tails: ";
        cin >> choice;

        // Check for valid input
        if (choice != 1 && choice != 2) {
            cout << "Invalid choice. Please enter 1 for Heads or 2 for Tails." << endl;
            continue;
        }

        // Generate a random number (0 or 1)
        int toss = rand() % 2;

        // Display the result of the coin toss
        if (toss == 0) {
            cout << "Result: Heads!" << endl;
        } else {
            cout << "Result: Tails!" << endl;
        }

        // Ask the user if they want to toss again
        cout << "Do you want to toss again? (y/n): ";
        cin >> again;

        // Validate user input for 'again'
        if (again != 'y' && again != 'Y' && again != 'n' && again != 'N') {
            cout << "Invalid choice. Exiting the program." << endl;
            break;
        }
    }

    cout << "Thank you for playing the Coin Toss Simulator!" << endl;
    return 0;
}
