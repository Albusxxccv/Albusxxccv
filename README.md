#include <iostream>
using namespace std;

void sumArray(), findMax(), reverseArray(), countEvenOdd();

int main() {
    int choice;
    do {
        cout << "Menu:\n1. Sum\n2. Max\n3. Reverse\n4. Even/Odd\n5. Exit\nChoice: ";
        cin >> choice;
        switch(choice) {
            case 1: sumArray(); break;
            case 2: findMax(); break;
            case 3: reverseArray(); break;
            case 4: countEvenOdd(); break;
        }
    } while (choice != 5);
    return 0;
}

void sumArray() {
    float arr[6], sum = 0;
    for (int i = 0; i < 6; ++i) cin >> arr[i], sum += arr[i];
    cout << "Sum: " << sum << endl;
}

void findMax() {
    int arr[7], max;
    for (int i = 0; i < 7; ++i) cin >> arr[i];
    max = arr[0];
    for (int i = 1; i < 7; ++i) if (arr[i] > max) max = arr[i];
    cout << "Max: " << max << endl;
}

void reverseArray() {
    int arr[5];
    for (int i = 0; i < 5; ++i) cin >> arr[i];
    for (int i = 4; i >= 0; --i) cout << arr[i] << " ";
    cout << endl;
}

void countEvenOdd() {
    int arr[10], even = 0, odd = 0;
    for (int i = 0; i < 10; ++i) {
        cin >> arr[i];
        (arr[i] % 2 == 0) ? ++even : ++odd;
    }
    cout << "Even: " << even << " Odd: " << odd << endl;
}
