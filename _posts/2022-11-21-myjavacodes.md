---
title: "My java codes."

date: 2022-11-21 00:00:00 -500
categories: [java, code,practice]
tags: [java,codes]
---
# My java codes

Hello everyone,
this is my first post showing off my java skills.

this is my first java code i ever wrote

```java
//java program for to print the pattern of stars
import java.util.Scanner;

public class test1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of rows: ");
        int n = sc.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

it might be good or it might be bad i dont really know.

Anyways you can find these codes on my [github](https://github.com/ifsvivek/Codes).

Anyways here is what i was working few days back

```java
/*Sorting a 2D Array according to 
values in any given column in Java*/

import java.util.Scanner;

public class p27 {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows");
        int n = sc.nextInt();
        System.out.println("Enter the number of columns");
        int m = sc.nextInt();
        int a[][] = new int[n][m];
        System.out.println("Enter the elements");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                a[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m - 1; j++) {
                for (int k = j + 1; k < m; k++) {
                    if (a[i][j] > a[i][k]) {
                        int temp = a[i][j];
                        a[i][j] = a[i][k];
                        a[i][k] = temp;
                    }
                }
            }
        }
        System.out.println("The sorted ar  ray is");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

if you have any questions you can contact my PA on [Twitter](https://twitter.com/spyscientist03).

so yeah, let see how long will i continues to write these post
, anyhow no one will see this.

this was me Vivek Sharma.

**LINKS**

* [Twitter](https://twitter.com/ifsvivek/){:target="_blank"}
* [Github](https://github.com/ifsvivek/){:target="_blank"}
* [Youtube](https://www.youtube.com/@ifsvivek){:target="_blank"}

cyaa...
