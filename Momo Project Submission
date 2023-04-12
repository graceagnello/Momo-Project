#include <iostream>
using namespace std;

int main() {
    int pin = 0000; // Default pin
    int balance = 1000; // Default balance
    int attempts = 0; // Counter for wrong attempts
    int option; // To store menu option chosen by user
    
    while (attempts < 3) {
        cout << "Please enter your 4-digit PIN: ";
        int userInput;
        cin >> userInput;
        
        if (userInput == pin) {
            cout << "Authentication successful!\n";
            
            // Display menu
            cout << "Menu:\n";
            cout << "1. Reset/change PIN\n";
            cout << "2. Check balance\n";
            cout << "3. Send money\n";
            cout << "4. Exit\n";
            
            cout << "Please select an option: ";
            cin >> option;
            
            switch(option) {
                case 1: // Reset/change PIN
                    cout << "Please enter new 4-digit PIN: ";
                    cin >> pin;
                    cout << "PIN changed successfully!\n";
                    break;
                
                case 2: // Check balance
                    cout << "Your balance is: " << balance << endl;
                    break;
                
                case 3: // Send money
                    cout << "Please enter amount to send: ";
                    int amount;
                    cin >> amount;
                    if (amount > balance) {
                        cout << "Insufficient balance.\n";
                    } else {
                        balance -= amount;
                        cout << amount << " sent successfully!\n";
                    }
                    break;
                
                case 4: // Exit program
                    cout << "Exiting program.\n";
                    return 0;
                
                default: // Wrong menu option chosen
                    cout << "Invalid option. Please try again.\n";
                    break;
            }
            
        } else {
            attempts++;
            cout << "Authentication failed. Please try again.\n";
        }
    }
    
    // If we reach this point, user has failed authentication 3 times
    cout << "Too many failed attempts. Program will exit now.\n";
    return 0;
}
