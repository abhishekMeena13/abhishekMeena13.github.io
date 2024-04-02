# Day 2 of 100 days of code!


Today we are making a _simple_  calculator in c++

It's so simple I dont even need to explain it!

```c++
#include <iostream>

using namespace std;

int calculate(int type, int num1, int num2){
    int answer;
    if (type == 1){
        answer= num1+num2;
    } else if (type ==2){
        answer= num1 - num2;
    } else if (type ==3){
        answer= num1*num2;
    } else if (type == 4){
        answer = num1/num2;
    }
    return answer;
}


int main(){
    cout << "Calculator!";

    int num1, num2, type;
    cout << "Please enter number 1: ";
    cin >> num1;
    cout << "Please enter number 2: ";
    cin >> num2;
    cout << "Press 1 for - Addition\n" << "Press 2 for - subtraction\n" << "Press 3 for - multiplication\n"<< "Press 4 for division: ";
    cin >> type;
    int answer;
    answer = calculate(type, num1, num2);
    cout << answer;



}

```

Bye, see you tommorow!
