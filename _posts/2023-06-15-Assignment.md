---
title: "Assignment - 1 BPOPS103."

date: 2023-06-16 00:00:00 -500

categories: [c, code, college]

tags: [c, codes, college]
---
# Assignment-1 BPOPS103

## 1. Sum of 2 numbers

```c
#include <stdio.h>

int main() {
    int num1, num2;
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);
    printf("The sum of %d and %d is %d\n", num1, num2,num1+num2);
    return 0;
}
```

## 2. Area and perimeter of a circle

```c
#include <stdio.h>

int main() {
    int rad;
    printf("Enter the radius: ");
    scanf("%d", &rad);
    printf("Area: %0.2f\n", 3.14*rad*rad );
    printf("Perimter: %0.2f", 2*3.14*rad );
    return 0;
}
```

## 3. Area and perimeter [2*(l+b)] of a rectangle

```c
#include <stdio.h>

int main() {
    float l,b;
    printf("Enter L and B: ");
    scanf("%f %f", &l, &b);
    printf("Area: %0.2f\n", l*b );
    printf("Perimter: %0.2f", 2*(l*b) );
    return 0;
}
```

## 4. Calculation of simple interest : ptr/100

```c
#include <stdio.h>

int main() {
    float p,t,r;
    printf("Enter P, T and R: ");
    scanf("%f%f%f", &p, &t,&r);
    printf("SI= %0.2f\n", (p*t*r)/100 );
    return 0;
}
```

## 5. Convert temperature in degree to Fahrenheit

```c
#include <stdio.h>

int main() {
    float c;
    printf("Enter the celsius: ");
    scanf("%f", &c);
    printf("Fahrenheit: %0.2f\n",c*9/5+32);
    return 0;
}
```

## 6. Convert temperature in degree to Fahrenheit

```c
#include <stdio.h>

int main() {
    float c;
    printf("Enter the celsius: ");
    scanf("%f", &c);
    printf("Fahrenheit: %0.2f\n",c*9/5+32);
    return 0;
}
```

## 7. Greatest of 2 numbers

```c
#include <stdio.h>

int main() {
    int a,b;
    printf("Enter Two Number: ");
    scanf("%d%d",&a,&b);
    if(a>b){
        printf("%d is Greater",a);
    }
    else{
        printf("%d is Greater",b);
    }
    return 0;
}
```

## 8. To check a number is odd or even

```c
#include <stdio.h>

int main() {
    int a;
    printf("Enter the Number: ");
    scanf("%d",&a);

    if(a%2==0){
        printf("%d is Even",a);
    }
    else{
        printf("%d is Odd",a);
    }
    return 0;
}
```

## 9. Greatest of 3 numbers

```c
#include <stdio.h>

int main() {
    int a,b,c;
    printf("Enter Two Number: ");
    scanf("%d%d%d",&a,&b,&c);
    if(a>b && a>c){
        printf("%d is Greatest",a);
    }
    else if(b>c) {
        printf("%d is Greatest",b);
    }
    else{
        printf("%d is Greatest",c);
    }
    return 0;
}
```

## 10. Sum of n natural numbers

```c
#include <stdio.h>

int main() {
    int n, sum = 0;
    printf("Enter a positive integer: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    printf("The sum of the first %d natural numbers is %d\n", n, sum);
    return 0;
}
```
