---
title:  "My C++ codes."

date: 2022-11-30 00:00:00 -500
categories: [c++, code,practice]
tags: [c++,codes]
render_with_liquid: false
---
Hello everyone this is my second post, hoping y'all read the first post

So here this is my first c++ code I wrote

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a, b, c;
    cout << "Enter the value of a,b,c:";
    cin >> a >> b >> c;
    if (a > b && a > c)
    {
        cout << "a is greater";
    }
    else if (b > a && b > c)
    {
        cout << "b is greater";
    }
    else
    {
        cout << "c is greater";
    }
    return 0;
}
```

It was a very simple code but it took me 2 days to write this dumb code

It is actually funny how normal people will write a code that is print hello world, and I am here writing a code with condition statements.
Looking back If I had written hello world it wouldn't have taken me 2 days to write my first code, but hey what we can do. It is what it is,

This was my third code and it was a calculator

```cpp
#include<iostream>
using namespace std;
int main(){
    int a,b,c;
    cout<<"Enter two numbers: ";
    cin>>a>>b;
    cout<<"Choose an operator: ";
    char op;
    cin>>op;
    if(op=='+'){
        c=a+b;
        cout<<"The sum is: "<<c;
    }
    else if(op=='-'){
        c=a-b;
        cout<<"The difference is: "<<c;
    }
    else if(op=='*'){
        c=a*b;
        cout<<"The product is: "<<c;
    }
    else if(op=='/'){
        c=a/b;
        cout<<"The quotient is: "<<c;
    }
    else{
        cout<<"Invalid operator";
    }
}
```

It works and it's simple
But this is what I wrote after learning to use arrays

```cpp
#include<iostream>
using namespace std;
int main(){
    int a[10],b[10],c[10],i,j,k,n,m,sum=0;
    cout<<"Enter the number of elements in first array: ";
    cin>>n;
    cout<<"Enter the elements of first array: ";
    for(i=0;i<n;i++)
        cin>>a[i];
    cout<<"Enter the number of elements in second array: ";
    cin>>m;
    cout<<"Enter the elements of second array: ";
    for(i=0;i<m;i++)
        cin>>b[i];
    for(i=0;i<n;i++)
        for(j=0;j<m;j++)
            c[i+j]=a[i]+b[j];
    cout<<"The elements of resultant array are: ";
    for(i=0;i<n+m;i++)
        cout<<c[i]<<" ";
    cout<<endl;
    for(i=0;i<n+m;i++)
        sum=sum+c[i];
    cout<<"The sum of all elements is: "<<sum;
    return 0;
}
```

Yeah. It is a calculator but with arrays this time.
i guess wthat its for today.
cyaa in next post.
