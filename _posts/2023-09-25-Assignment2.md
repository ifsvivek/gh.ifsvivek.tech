---
title: "Assignment - 2 BPOPS103"
date: 2023-09-25 00:00:00 -500
categories: [c, code, college]
tags: [c, codes, college]
---
# Assignment-2 BPOPS103

## 1.	Write a  C program to read N integers into an array A and to

    * Find the sum of odd numbers
    * Find the sum of even numbers
    * Find the average of all numbers

```c
#include <stdio.h>

int main(){
    int N;

    printf("Enter the number of elements: ");
    scanf("%d", &N);

    int A[N], sumOdd = 0, sumEven = 0, totalSum = 0, oddCount = 0, evenCount = 0;

    printf("Enter %d integers:\n", N);
    for (int i = 0; i < N; i++){
        scanf("%d", &A[i]);
        totalSum += A[i];

        if (A[i] % 2 == 0){
            sumEven += A[i];
            evenCount++;
        }
        else{
            sumOdd += A[i];
            oddCount++;
        }
    }

    float average = (float)totalSum / N;
    printf("Sum of odd numbers: %d\nSum of even numbers: %d\nAverage of all numbers: %.2f\n", sumOdd, sumEven, average);
    return 0;
}
```

## 2. Write a program to replace each constant in a string with the next one except letter ‘z’ ‘Z’ and ‘a’, ‘A’. Thus the string “programming in C is fun” should be modified as “qsphsannjoh jo D jt gvo”.

```c
#include <stdio.h>

int main(){
    char input[100]="programming in C is fun", output[100];
    int i = 0;
    while (input[i] != '\0'){
        char c = input[i];

        if ((c >= 'a' && c < 'z') || (c >= 'A' && c < 'Z')){
            output[i] = c + 1;
        }
        else if (c == 'z' || c == 'Z'){
            output[i] = c - 25;
        }
        else{
            output[i] = c;
        }
        i++;
    }

    output[i] = '\0';
    printf("Modified string: %s", output);
    return 0;
}
```

## 3. Write a C program to swap 2 numbers using global variable concept and pass by reference concept.

```c
#include <stdio.h>

void swap(int *a, int *b){
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main(){
    int num1, num2;

    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    printf("Original numbers: num1 = %d, num2 = %d\n", num1, num2);
    swap(&num1, &num2);

    printf("After swapping: num1 = %d, num2 = %d\n", num1, num2);
    return 0;
}
```

## 4. Write a C program to print all the prime numbers in a given range. Use functions.

```c
#include <stdio.h>

int isPrime(int n){
    if (n <= 1)
        return 0;
    for (int i = 2; i * i <= n; i++)
    {
        if (n % i == 0)
            return 0;
    }
    return 1;
}

int main(){
    int n1, n2;
    printf("Enter the first number: ");
    scanf("%d", &n1);
    printf("Enter the second number: ");
    scanf("%d", &n2);

    printf("Prime numbers between %d and %d: ", n1, n2);
    for (int i = n1; i <= n2; i++){
        if (isPrime(i))
            printf("%d ", i);
    }
    printf("\n");
    return 0;
}
```
