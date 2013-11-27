Part 1
======
Watch “Foundations of Programming: Fundamentals” at Lynda.com and then answer
the following questions:

1. Imagine asking a friend to meet you at a restaurant. What instructions would 
   a computer program need that your friend would not in order to understand how
   to get there?
   
-A computer program would require far more instructions than one’s friend. Each step (many of which humans take for granted) must be broken down into its smallest parts. In the case of a Google driverless car, for example, many thousands (perhaps hundreds of thousands) of lines of code may be required to complete this seemingly simple task. 

2. What is the difference between source code and machine code? What does the
   CPU do? Where are instructions and data stored?
   
   -Machine code provides instructions directly to the CPU. However, it is extremely difficult for humans to read. Source code is the language that people use to write programs. It is more easily understood by humans and is compiled or interpreted to create machine code for the computer. 
   -The CPU is the central processing unit, the brain of the computer or mobile device. It processes the machine code instructions. 
   -For long term storage, they are normally on the hard drive (or SSD drive) though they may be stored elsewhere, as on a flash drive, DVD, or in the Cloud (on a server elsewhere). When the program is run, they are copied into the RAM. In a compiled language, the instructions are stored as machine code. In an interpreted language, they are stored as source code and only converted to machine code when the program is run.

3. What is an IDE and why is it useful?

-An IDE is an integrated development environment. It includes a number of features that assist in the writing of code, such as line numbers, color-coding, and checking syntax as one types. 

4. What kind of a language is Objective-C? Why do you think we use it for making
   device specific applications? Why wouldn't we want to use an interpreted
   language for making iPhone and iPad apps?
   
   -Objective-C is a compiled language.
   -In a device-specific context, the versatility of an interpreted language is not necessary because the program only needs to run on a single platform. Using a compiled language allows the program to be tailored to the specific CPU and ready to run immediately, thereby increasing its speed. Additionally, the programs’ codes can be kept private. 
   -IPhone and iPad apps would not benefit from the cross-platform flexibility that is the biggest advantage of an interpreted language, yet such a language would slow them down and make their program codes public. A compiled language sacrifices flexibility that isn’t necessary anyway in exchange for speed and privacy, which are desirable. 



Part Two
========
Read chapters *1* through *11* of The Big Nerd Ranch book and complete all the
exercises.


Challenge Chapter Three:
#include <stdio.h>

int main(int argc, const char * argv[])
{
    // declare variables
    float salt = 37.45;
    float pepper = 11.22;
    
    // declare a variable that is their sum
    double saltNpepper = salt + pepper;
    
    // print result
    printf("The sum of salf and pepper is %f.\n", saltNpepper);
    
    // finish
    return 0;
}


Challenge Chapter Four
“The first expression is true.” 


Challenge Chapter Five
#include <stdio.h>

float remainingAngle(float firstAngle, float secondAngle)
{
    float thirdAngle = 180 - firstAngle - secondAngle;
    return thirdAngle;
}

int main(int argc, const char * argv[])
{
    float angleA = 30.0;
    float angleB = 60.0;
    float angleC = remainingAngle(angleA, angleB);
    printf("The third angle is %.2f\n", angleC);
    return 0;
}


Challenge Chapter Six
#include <stdio.h>
#include <math.h>

int main(int argc, const char * argv[])
{
    printf("The sine of 1 radian is %.3f.\n", sin(1.0));
    return 0;
}



Challenge Chapter Seven
#include <stdio.h>

int main(int argc, const char * argv[])
{
   
    for (int i = 99; i > -1; i--) {
        printf("%d\n", i);
        if (i % 5 == 0) {printf("Found one!\n");
        }
    }
        return 0;
}



Challenge Chapter Eight
1.
#include <stdio.h>

int main(int argc, const char * argv[])
{    
    printf("A float is %zu bytes.\n", sizeof(float *));
    return 0;
}

2. The shortest number that a short can hold is -32,768.
The largest is 32,767.
The largest number that an unsigned short can hold is 65,535.


Challenge Chapter Ten

#include <stdio.h>
#include <time.h>
int main(int argc, const char * argv[])
{
    struct tm now;
    long secondsSince1970 = time(NULL);
    printf("It has been %ld seconds since 1970\n", secondsSince1970);
    long FutureTimeinSeconds = secondsSince1970 + 4000000;
    printf("In four million seconds there will have been %ld seconds since 1970.\n", FutureTimeinSeconds);
    
    localtime_r(&FutureTimeinSeconds, &now);
    int month = now.tm_mon + 1;
    int year = now.tm_year + 1900;
    printf("The date in four million seconds will be %d-%d-%d\n", month, now.tm_mday, year);
    return 0;
}










