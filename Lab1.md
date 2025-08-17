# 📘 Lab1.md

## Problem 1: Hello World
### Program
```c
#include <stdio.h>
int main() {
    printf("Hello, World!\n");
    return 0;
}
```
### Output
``` 
Hello, World!
```
## Problem 2: Ask user their name and age
### Program
```c
#include <stdio.h>
int main(){
    int age;
    char name[50];

    printf("Enter Your name: ");
    scanf("%s",&name);
    printf("Enter your age: ");
    scanf("%d",&age);

    printf("Name: %s\n Age: %d",name,age);
    return 0;
}
```
## Output
```
Enter Your name: Anshul
Enter your age: 18
Name: Anshul
Age: 18
```
# Problem 3: Take 2 numbers from user and return their sum
## Program
```c

#include <stdio.h>
int main(){
    int a;
    int b;
    int sum;
    printf("Enter Nums: ");
    scanf("%d %d" ,&a,&b);
    
    sum=a+b;
    printf("Sum: %d",sum);
    return 0;
}


```
## Output
```
Enter Nums: 23 17
Sum: 40
```
# 📌Conclusion
- Learnt printf, scanf and basics.
- Understood how code in C works.


