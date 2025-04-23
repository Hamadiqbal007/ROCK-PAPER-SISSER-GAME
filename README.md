#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0)); 
    int i = 1, user;

    while (i == 1) {
        int num = rand() % 3;

        cout << "\tWELCOME TO ROCK PAPER SCISSORS GAME DEVELOPED BY ZEROES!" << endl;
        cout << "\tGAME INSTRUCTIONS:" << endl;
        cout << "\t'0' FOR ROCK" << endl;
        cout << "\t'1' FOR SCISSORS" << endl;
        cout << "\t'2' FOR PAPER" << endl;
        cout << "\tRock beats Scissors, Scissors beats Paper, Paper beats Rock." << endl;
        cout << "Enter your choice: ";
        cin >> user;

        if (user >= 3 || user < 0) {
            cout << "Invalid input! Enter only 0, 1, or 2: ";
            cin >> user;
        }

        if (user == num) {
            cout << "It's a TIE!" << endl;
        } else if (user == 0) {
            if (num == 1) {
                cout << "You WIN! Rock beats Scissors." << endl;
            } else {
                cout << "You LOSE! Paper covers Rock." << endl;
            }
        } else if (user == 1) {
            if (num == 0) {
                cout << "You LOSE! Rock smashes Scissors." << endl;
            } else {
                cout << "You WIN! Scissors cut Paper." << endl;
            }
        } else if (user == 2) {
            if (num == 0) {
                cout << "You WIN! Paper covers Rock." << endl;
            } else {
                cout << "You LOSE! Scissors cut Paper." << endl;
            }
        }

        cout << "Do you want to play again? Enter '1' for Yes or '0' for No: ";
        cin >> i;
    }

    return 0;
}
