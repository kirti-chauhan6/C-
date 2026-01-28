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







write a c++  program   to read and display elements of an array

#include <iostream>
using namespace std;

int main() {
    int n;
    int arr[100];

    cout << "Enter the number of elements: ";
    cin >> n;

    cout << "Enter the elements of the array:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    cout << "The elements of the array are:\n";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }

    return 0;
}




#include <iostream>
using namespace std;

int main() {
    int n, sum = 0;
    int arr[100];

    cout << "Enter the number of elements: ";
    cin >> n;

    cout << "Enter the elements of the array:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
        sum += arr[i];   // add each element to sum
    }

    cout << "Sum of all elements in the array = " << sum;

    return 0;
}




write a C++ program to  find  the sum of all elements in an array

#include <iostream>
using namespace std;

int main() {
    int n, sum = 0;
    int arr[100];

    cout << "Enter the number of elements: ";
    cin >> n;

    cout << "Enter the elements of the array:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
        sum += arr[i];   // add each element to sum
    }

    cout << "Sum of all elements in the array = " << sum;

    return 0;
}




write a code to copy one array  into another

#include <iostream>
using namespace std;

int main() {
    int n;
    int arr1[100], arr2[100];

    cout << "Enter the number of elements: ";
    cin >> n;

    cout << "Enter elements of the first array:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr1[i];
    }

    // Copying elements from arr1 to arr2
    for (int i = 0; i < n; i++) {
        arr2[i] = arr1[i];
    }

    cout << "Elements of the second array after copying:\n";
    for (int i = 0; i < n; i++) {
        cout << arr2[i] << " ";
    }

    return 0;
}





Write a C++ program to read and display a 2D array (matrix).

#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    int matrix[10][10];

    cout << "Enter number of rows and columns: ";
    cin >> rows >> cols;

    cout << "Enter elements of the matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "The matrix is:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}



#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    int matrix[10][10];

    cout << "Enter number of rows and columns: ";
    cin >> rows >> cols;

    cout << "Enter elements of the matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Matrix elements in row-wise order:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}



Write a C++ program to print all elements of a matrix in column-wise order.


#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    int matrix[10][10];

    cout << "Enter number of rows and columns: ";
    cin >> rows >> cols;

    cout << "Enter elements of the matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Matrix elements in column-wise order:\n";
    for (int j = 0; j < cols; j++) {
        for (int i = 0; i < rows; i++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}

