// Buckley - Hacking Program.cpp : This file contains the 'main' function. Program execution begins and ends there.
// Nicholas Buckley 11.4.18

#include "pch.h"
#include <iostream>
#include <string>

using namespace std;

// Declaring Functions
void normalTransaction(int x, int y); // this function takes argument by copies to execute
void hackedTransaction(int& x, int& y); // this function takes argument by reference to execute

int main()
{
	int coffee = 500; // Starting bank amount of coffee shop
	int terrorist = 1000000; // Starting bank amount of Terrorist Organization
	string execute;
	// Displaying Original Bank Balances for Coffee Shop and Terrorist Organization
	cout << "Bank Balance - \n";
	cout << "Joe's Coffee Shop: $" << coffee << "\n"; // Coffee Shop balance printed
	cout << "Terrorist Organization: $" << terrorist << "\n\n"; // Terrorist Organization printed


	// Displaying a normal trasaction with function normalTransaction()
	cout << "Transaction Complete - \n";
	// Calling function normalTransaction with coffee as int x and terrorist as int y
	normalTransaction(coffee, terrorist);
	cout << "Joe's Coffee Shop: $" << coffee << "\n"; // Coffee Shop balance printed
	cout << "Terrorist Organization: $" << terrorist << "\n\n"; // Terrorist Organiztion balance printed

	cout << "Preparing Hacking Program...\n";
	cout << "Hacking Program ready to execute...\n\n";
	cout << "Enter 'Hack' to execute program:\n\n";
	cin >> execute;

	cout << "\nTransaction Complete - \n";
	// Calling function hackedTransaction with coffee as int x and terrorist as int y
	hackedTransaction(coffee, terrorist);
	cout << "Joe's Coffee Shop: $" << coffee << "\n"; // Coffee Shop balance printed
	cout << "Terrorist Organization: $" << terrorist << "\n\n"; // Terrorist Organiztion balance printed

	system("pause"); // System Paused

	return 0; // Return zero for error test
}

// The creation of function normalTransaction()
void normalTransaction(int x, int y)
{
	// coffee set as x
	// terrorist set as y

	int change = x; // temp is assigned coffee balance (x)
	x = y; // x is set to y or coffee is set to terrorist
	y = change; // y is set to the value temp holds (x)

	// Only a temporary change
}

// The creation of function hackedTransaction()
void hackedTransaction(int& x, int& y)
{
	// coffee is set to x as a reference
	// terrorist is set to y as a reference

	int change = x; // temp is assigned coffee balance (x)
	x = y; // x is set to y or coffee is set to terrorist
	y = change; // y is set to the value temp holds (x)

	// Values are then changed
}
