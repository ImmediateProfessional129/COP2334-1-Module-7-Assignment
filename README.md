# COP2334-1-Module-7-Assignment
This is a repository link of the COP2334-1 Module 7 Assignment

// This program is designed to calculate the total number of sales for the highest selling salsa between 5 types of salsa brands and flavors.

// Include the header files.
#include <iostream>
#include <string>
using namespace std; // Using standard namespace.

int main() { // Main function.
    const int SIZE = 5; // Declare a constant integer variable SIZE and initialize it to 5.
    string salsa[SIZE] = {"Mateo's mild", "Herdez medium", "Mission sweet", "La Victoria hot", "Newman's Own zesty"}; // Declare an array of strings named salsa and initialize it with the names of the 5 salsa flavors.
    int jars[SIZE]; // Declare an array of integers named jars.
    int total = 0; // Declare an integer variable named total and initialize it to 0.
    int highest_in_sales = 0; // Declare an integer variable named highest_in_sales and initialize it to 0.
    int lowest_in_sales = 0; // Declare an integer variable named lowest_in_sales and initialize it to 0.
    for (int i = 0; i < SIZE; i++) { // Use a for loop to iterate through the array of strings salsa.
    cout << "Enter the number of jars that sold out the most. " << salsa[i] << ": "; // Prompt the user to enter the number of jars that sold out the most for each salsa flavor.
    cin >> jars[i]; // Read the user's input and store it in the corresponding element of the array jars.
    while (jars[i] < 0) { // Use a while loop to validate the user's input.
      cout << "Please enter a positive number: "; // Prompt the user to enter a positive number.
      cin >> jars[i]; // Read the user's input and store it in the corresponding element of the array jars.
    }
      total += jars[i]; // Add the value of the current element of the array jars to the variable total.
      if (jars[i] > jars[highest_in_sales]) { // Use an if statement to compare the value of the current element of the array jars with the value of the variable highest_in_sales.
      highest_in_sales = i;
    }
      if (jars[i] < jars[lowest_in_sales]) { // Use an if statement to compare the value of the current element of the array jars with the value of the variable lowest
      lowest_in_sales = i;
    }
  }
  cout << "Salsa Sales Report" << endl; // Print the header of the sales report.
  cout << "------------------" << endl; // Print a line of dashes to separate the header from the rest of the report.
  for (int i = 0; i < SIZE; i++) { // Use a for loop to iterate through the array of strings salsa.
    cout << salsa[i] << ": " << jars[i] << " jars" << endl; // Print the name of the current salsa flavor and the number of jars that sold out the most for that flavor.
  }
  cout << "Total Sales: " << total << " jars" << endl; // Print the total number of jars that sold out the most.
  cout << "Highest Selling Product: " << salsa[highest_in_sales] << endl; // Print the name of the salsa flavor that sold out the most.
  cout << "Lowest Selling Product: " << salsa[lowest_in_sales] << endl; // Print the name of the salsa flavor that sold out the least.
  return 0; // Return 0 to indicate successful program execution.
}  
