# C-
Pointer 


#include <iostream>
using namespace std;


int globalVar = 10;

int main() {
   
    int localVar = 20;

    
    int* heapVar = new int(30);

    cout << "Address of Global Variable (Global/Static Memory): "
         << &globalVar << endl;

    cout << "Address of Local Variable (Stack Memory): "
         << &localVar << endl;

    cout << "Address of Dynamically Allocated Variable (Heap Memory): "
         << heapVar << endl;

             
    delete heapVar;

    return 0;
}





//Write a function square(int) and call it:

Normally

Using a function pointer



#include <iostream>
using namespace std;

// Function definition
int square(int x) {
    return x * x;
}

int main() {
    int num = 5;

    // 1️⃣ Normal function call
    cout << "Normal call result: " << square(num) << endl;

    // 2️⃣ Function pointer declaration
    int (*funcPtr)(int);

    // Assign function address to pointer
    funcPtr = square;

    // Call function using function pointer
    cout << "Function pointer call result: " << funcPtr(num) << endl;

    return 0;
}





#include <iostream>
using namespace std;

int main() {
    int x = 10;        // Variable declaration
    int* ptr = &x;    // Pointer storing address of x

    cout << "Value of variable x: " << x << endl;
    cout << "Address of variable x: " << &x << endl;
    cout << "Value stored in pointer ptr: " << ptr << endl;

    return 0;
}











#include <iostream>
using namespace std;

int main() {
    int a = 25;        // Original variable
    int* ptr = &a;    // Pointer storing address of a
    int b;            // Third variable

    // Copy value using dereferencing
    b = *ptr;

    cout << "Value of a: " << a << endl;
    cout << "Address stored in ptr: " << ptr << endl;
    cout << "Value copied into b using dereferencing: " << b << endl;

    return 0;
}














#include <iostream>
using namespace std;

int main() {
    // Create dynamic integer
    int* ptr = new int(10);

    cout << "Initial value: " << *ptr << endl;

    // Modify value using pointer
    *ptr = 25;

    cout << "Modified value: " << *ptr << endl;

    // Delete dynamically allocated memory
    delete ptr;

    // Optional: Avoid dangling pointer
    ptr = nullptr;

    return 0;
}
