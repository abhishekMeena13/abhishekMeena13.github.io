# How to Create a Simple Billing System in C++

## Introduction

Hey there! It's Abhishek here again! Today, I'm going to guide you through creating a simple billing system in C++. Have you ever been to a supermarket and received an invoice after checkout? Well, we're going to recreate a basic version of that in C++!

## Requirements

All you need is a bit of brainpower and some familiarity with C++.

## Let's Get Started!

You can use your favorite code editor! First, let's include two essential libraries:

```cpp
#include <iostream>
#include <string>
using namespace std;
```

We'll also use using namespace std; to avoid typing std:: repeatedly.

```cpp
class Item {
public:
    int id;
    string name;
    int price;
};

```
Here, we've defined a class called Item, which serves as the blueprint for our invoice. It has three member variables: id, name, and price.

Now, let's create a function to display the invoice:

```cpp
void display(Item items[], int size, string customerName) {
```

This line declares a function named display that takes three parameters:

items[]: An array of Item objects representing the items to be displayed.

size: An integer representing the size of the array.

customerName: A string representing the name of the customer.

```cpp
int total = 0;
```
This line declares an integer variable total and initializes it to 0. This variable will store the total price of all items in the invoice.


```cpp
system("cls"); // Clear the screen
```

This line uses the system function to execute a command that clears the console screen. This helps in displaying the invoice cleanly.


```cpp
    cout << "\n\n\n";
    cout << "\t Abhishek Store\n";
    cout << "\t------------------- \n";
    cout << "\n";
    cout << "Name: " << customerName << "\n";
```
These lines print the header of the invoice, including the store name and customer name, to the console.


```cpp
    for (int i = 0; i < size; i++) {

```
This line starts a for loop that iterates over each item in the items array.


```cpp
    cout << "ID: " << items[i].id << endl;
    cout << "Item name: " << items[i].name << endl;
    cout << "Price: " << items[i].price << endl;
    cout << "======================================" << endl;
```

These lines print the details of each item, including its ID, name, and price, to the console. They also print a separator line between items.


```cpp
        total += items[i].price;
```

This line adds the price of the current item to the total variable, calculating the cumulative total price of all items.


```cpp
    }

    cout << "Total: " << total << endl;
    cout << "\n\n";
    cout << "Thanks for visiting the Abhishek Store!\n";
}
```

These lines print the total price of all items and a closing message to the console, indicating the end of the invoice display.


```cpp
int main() {

```
This line declares the main function, which serves as the entry point of the program.

```cpp
    cout << "Hello...\n";
    string customerName;
    int totalItems;

    cout << "Please enter your name: ";
    cin >> customerName;
    cout << "Please enter total items: ";
    cin >> totalItems;
    cout << "\n";

```

These lines prompt the user to enter their name and the total number of items for the invoice and store the inputs in the customerName and totalItems variables, respectively.

```cpp
    Item items[totalItems];

    for (int i = 0; i < totalItems; i++) {
        items[i].id = i + 1;
        cout << "Enter item " << i + 1 << " name: ";
        cin >> items[i].name;
        cout << "Enter price: ";
        cin >> items[i].price;
    }

```
These lines declare an array of Item objects named items and populate it with details entered by the user for each item in the invoice.



```cpp
    display(items, totalItems, customerName);

    return 0;
}

```

This line calls the display function to display the invoice, passing the items array, totalItems, and customerName as arguments. Finally, the main function returns 0 to indicate successful execution of the program.

And that's it! You've created a simple billing system in C++. Feel free to customize and enhance it further based on your requirements.

This is Abhishek signing off! Adieu!!


