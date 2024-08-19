# Experiment 8 :- To study and implement C++ 2D Array - Matrices

## AIM: -
To learn how to implement 2D arrays (Matrices) in C++ and its operations like addition, multiplcation , diagonal addition and comparing 2 rows 

## Software: - VS Code

## Theory: -

Arrays can be categorised in 2 types as follows: -
1. One dimensional array
2. Multi dimensional array

In this experiments we are going to learn about 2 dimensional arrrays also known as matrices. Matrices consist of rows and columns each consisting of 1 dimension array therfore making them 2D arrays. 

### Basic Operations on Matrices: - 

1. Taking Inputs for the matrix elements and storing them in the matrix.
2. Taking transpose of a matrix and storing it in a new matrix.
3. Addition of two matrices and storing the sum in a new matrix.
4. Subtraction of two matrices and storing the difference in a new matrix.
5. Multiplication of two matrices and storing the product in a new matrix.

### Code - 

```
#include <iostream>
using namespace std;

int main() {
int r, c;

//  Taking matrix dimensions as input
cout << "Enter the number of rows: ";
cin >> r;
cout << "Enter the number of columns: ";
cin >> c;

// Declaring matrices
int m1[r][c], m2[r][c], sum[r][c], prod[r][c];

// Input elements for the first matrix
cout << "Enter the elements of the first matrix:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << "Element [" << i + 1 << "][" << j + 1 << "]: ";
        cin >> m1[i][j];
    }
}

// Input elements for the second matrix
cout << "Enter the elements of the second matrix:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << "Element [" << i + 1 << "][" << j + 1 << "]: ";
        cin >> m2[i][j];
    }
}

// Perform matrix addition
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        sum[i][j] = m1[i][j] + m2[i][j];
    }
}

// Perform matrix multiplication
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        prod[i][j] = 0;
        for (int k = 0; k < c; k++) {
            prod[i][j] += m1[i][k] * m2[k][j];
        }
    }
}

// Calculate diagonal sum of the first matrix
int diagSum = 0;
for (int i = 0; i < r; i++) {
    diagSum += m1[i][i];
}

// Check if the elements of the first row are equal to the elements of the second row in the first matrix
bool rowEqual = true;
for (int j = 0; j < c; j++) {
    if (m1[0][j] != m1[1][j]) {
        rowEqual = false;
        break;
    }
}

// Display the first matrix
cout << "\nThe first matrix is:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << m1[i][j] << " ";
    }
    cout << endl;
}

// Display the second matrix
cout << "\nThe second matrix is:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << m2[i][j] << " ";
    }
    cout << endl;
}

// Display the sum of the matrices
cout << "\nThe resultant matrix after addition is:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << sum[i][j] << " ";
    }
    cout << endl;
}

// Display the product of the matrices
cout << "\nThe resultant matrix after multiplication is:\n";
for (int i = 0; i < r; i++) {
    for (int j = 0; j < c; j++) {
        cout << prod[i][j] << " ";
    }
    cout << endl;
}


cout << "\nThe diagonal sum of the first matrix is: " << diagSum << endl;

// Display whether the first row is equal to the second row in the first matrix
if (rowEqual) {
    cout << "The first row and the second row are equal \n";
} else {
    cout << "The first row and the second row are equal \n";
}

return 0;
}
```

### Output: - 



### Conclusion: -

In this experimennt we learnt how to implement 2D arrays (matrices) and its operations like addition, multiplication, diagonal addition, transposing, etc in C++ programming language.
