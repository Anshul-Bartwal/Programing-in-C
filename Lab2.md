# 📘 Lab2.md
## Problem 1: Take length and width from user and enter perform some operations
### Program
```c
#include <stdio.h>
#include <stdbool.h>
int main(){
    int length;
    int width;
    int ldiv;
    float ldivi;
    int wdiv;
    int lwdiv;
    bool a;
    printf("Enter Length and Width:");
    scanf("%d %d",&length,&width);
    ldiv=length/3;
    ldivi=length/3.0;
    wdiv=width/2;
    lwdiv=length/width;
    a= ((width + length) / length > length / width);// a=0,1

    printf("Length/3: %d\n",ldiv);
    printf("Width/2: %d\n",wdiv);
    printf("Length/3.0: %f\n",ldivi);
    printf("Length/Width: %d\n",lwdiv);
    printf("(width + length) / length > length / width is (0:False , 1:True): %d",a);
    return 0; 
}
```
### Output
```
Enter Length and Width:10 3
Length/3: 3
Width/2: 1
Length/3.0: 3.333333
Length/Width: 3
(width + length) / length > length / width is (0:False , 1:True): 0
```
## Problem 2: WAP to compute 1/2π, where π = 3.1415926. Display the result up to 6 decimal places
### Program
```c
#include <stdio.h>
int main(){
    float ans;
    ans=1/(2*3.1415926);
    printf("Answer: %.6f",ans);//  %.6f .6 means six digits after .
    return 0;
}
```
### Output
```
Answer: 0.159155
```
## Problem 3://Q3.WAP in C to solve the quadratic equation:
### Program
```c
//quadratic fomrula: x= (-b(+-)*(b^2 - 4ac)^0.5)/2a
    #include <stdio.h>
    #include  <math.h>
    int main(){
        int a;
        int b;
        int c;
        float x1;
        float x2;
        printf("Equation: ax^2 + bx + c\n");
        printf("Enter a: b: c:");
        scanf("%d %d %d",&a,&b,&c);

        x1= ((-b)+sqrt((b*b)-(4*a*c)))/(2*a);
        x2= ((-b)-sqrt((b*b)-(4*a*c)))/(2*a);
        // printf("%d %d %d",a,b,c);
        //X2= ((-b)+sqrt(b*b -4*a*c))/2*a

        printf("x1,x2=%f %f ",x1,x2);
        return 0;
    }
```
### Output
```
Equation: ax^2 + bx + c
Enter a: b: c:1 0 -1
x1,x2=1.000000 -1.000000 
```
## Problem 4: If you run a 10 kilometer race in 43 minutes 30 seconds:
- Find your average time per km.
- Find your average speed in km/h.
### Program
```c
#include <stdio.h>
int main(){
    float km;
    int s;
    float min;
    float hr;
    float speed;
    float time;
    printf("Enter Distance:\n");
    scanf("%f",&km);
    printf("Enter Time(min , sec)\n");
    scanf("%f %d",&min,&s);
    min=min+(s/60);
    hr=min/60;
    
    speed=km/hr;
    time=1/speed;
    printf("Avg Time per km(in hr): %f\n",time);
    printf("Avg Speed in km/hr :  %f",speed);
    return 0;



}
```
### Output
```
Enter Distance:
10
Enter Time(min , sec)
43 30
Avg Time per km(in hr): 0.071667
Avg Speed in km/hr :  13.953489
```
## Problem 5:  WAP in C that takes five integers from the user and print their average
### Program
```c
#include <stdio.h>
int main(){
    int a;
    int b;
    int c;
    int d;
    int e;
    float avg;
    printf("Enter 5 numbers: ");
    scanf("%d %d %d %d %d",&a,&b,&c,&d,&e);
    avg=(a+b+c+d+e)/5;
    printf("AVG: %f\n",avg);
    return 0;
}
```
### Output
```
Enter 5 numbers: 1 4 2 5 2
AVG: 2.000000
```
## Problem 6: WAP in C that read two strings and join together using strcat() and finally print it
### Program
```c
#include  <stdio.h>
#include <string.h>
int main(){
    char s1 [50];
    char s2 [50];
    
    printf("Enter string 1(no spaces): "); // no space as scanf treats it as new variable
    scanf("%s",s1);
    printf("Enter string 2(no spaces): "); // no space as scanf treats it as new variable
    scanf("%s",s2);
    strcat(s1,s2); // concatenate last string to first string
    printf("%s",s1);
    return 0;

}
```
### Output
```
Enter string 1(no spaces): this 
Enter string 2(no spaces): string
thisstring
```
If we use spaces scanf will terminate at first space and will start scanning for new input after it and this messes up our program
```

Enter string 1(no spaces): this is string
Enter string 2(no spaces): thisis
```
Here "thisis" in line2 is the concatenation of "this" and "is" from line 1

# 📌Conclusion
- Learnt about arithematic operations
- Understood how scanf works
- Learnt string concatenation
- Used math library 
