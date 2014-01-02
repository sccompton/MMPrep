Challenge 3: Get Your Hands Dirty
=================================
Next up, find the Lynda.com video series entitled: “Objective-C Essential
Training”. Watch each video in the following list and answer the corresponding
question.

Section 1: Getting Started
==========================
[1.1] Installing the tools (4:42)
---------------------------------
You should already have Xcode installed, but you will need to register as an
Apple Developer.

Do you like cats?

-They're okay. 


[1.2] Creating your first application (11:28)
---------------------------------------------
Create your first application using the same steps Simon describes in the video.
Familiarize yourself with the Xcode environment, specifically notice how it can
be manipulated to display different helper tools and how it will attempt to fill
in your code as you type it.

[1.3] Updates to this course (3:31)
-----------------------------------
Why do you think it's important to be aware of the idiosyncracies with older
versions of Objective-C and to keep up with new features as they are added?

-It is good to be aware of previous versions because one may encounter programs, books, and websites that include code for previous versions. At the same, it is good to keep up on the latests developments to be able to work in the newest release of Xcode and take advantage of its new features and improvements. 


Section 2: Objective-C Basics
=============================
[2.1] The Objective-C language (4:11)
-------------------------------------
How did Objective-C become the language to learn if you want to make apps for
the iPhone and iPad?

-During his sojourn away from Apple, Steve Jobs founded NeXT Computer. In creating their NeXTSTEP operating system, they used Objective-C for all of their programming. When NeXT Computer was later purchased by Apple, the NeXTSTEP operating system became the basis for OSX. Objective-C is thus integral to OSX, which is built on two decades of layers and improvements in Objective-C. And iOS is built on top of OSX.


[2.2] The structure of an Objective-C program (6:15)
----------------------------------------------------
Create a new project. Go to the menu option `Xcode`, `Preferences`,
`Text Editing` and make sure *Line Numbers* is checked in the section marked
"Show." Then add comments describing the purpose of each auto-generated line in
the main.m file. For example on Line 17 I would write: 

```
NSLog(@"Hello, World!");  // instructs the console to output: Hello, World!
```


#import <Foundation/Foundation.h> //this code points to the foundation framework and tells the computer that the program can use this framework and all of the files within it

int main(int argc, const char * argv[]) //this is essential. it tells the computer where to begin and the program will crash without it
{ //opening curly brace marks the beginning of a unit of code which runs through to its closing brace

    @autoreleasepool { // this is to do with memory management
        
        // insert code here...
        NSLog(@"Hello, World!"); //instructs the console to output the phrase "Hello, World!”)"
        
    }
    return 0;  // returns 0 to end the program
} //final closing curly brace completes a section of code



[2.3] Compiling and running your code (8:37)
--------------------------------------------
Why might you build in one version of iOS but deploy in an older version?

-By building in the newest version of iOS, one can take advantage of the newest options and developments. But it is still desirable to make one’s program available to as many users as possible, even if they are using older versions of the operating system. 


Section 3: Program Flow
=======================
[3.1] Logging messages to the command line (6:07)
-------------------------------------------------
Following the example in the video, write a program that calculates and outputs
to the console the number of seconds in ten years. Copy and paste your code
here.

#import <Foundation/Foundation.h>

int main(int argc, const char * argv[])
{

    @autoreleasepool {
        
        
        int seconds = 60;
        int minutes = 60;
        int hours = 24;
        int days = 365;
        
        int secondsInTenYears = seconds * minutes * hours * days * 10;
        
        NSLog(@"There are %i seconds in ten years.", secondsInTenYears);
        
    }
    return 0;
}


[3.2] Writing conditional code (7:01)
-------------------------------------
Using Objective-C, create an integer variable called "day" that represents the
days of the week. Write an if statement that checks whether "day" is a weekend
day. If the day is a weekend day then have your program print a message saying
"Have a nice weekend!" and if it's not, print a message saying "I hope you're
having a good week!"

#import <Foundation/Foundation.h>

int main(int argc, const char * argv[])
{

    @autoreleasepool {
        
        int dayOfTheWeek = 1;
        
        if (dayOfTheWeek == 6 || dayOfTheWeek == 7) {
            NSLog(@"Have a nice weekend!");
        }
        else {
            NSLog(@"I hope you're having a good week!");
                  };
    }
    return 0;
}



[3.3] The switch statement (5:58)
---------------------------------
Create a variable called "hurricaneCategory" and a switch statement that prints
out a message describing a hurricane's category from 1-5.


#import <Foundation/Foundation.h>

int main(int argc, const char * argv[])
{

    @autoreleasepool {
        
        int hurricaneCategory = 4;
        
        switch (hurricaneCategory) {
            case 1:
                NSLog(@"This is a small hurricane. Winds are 74-95 mph.");
                break;
            case 2:
                NSLog(@"This is a medium hurricane. Winds are 96-110 mph");
            case 3:
                NSLog(@"This is a large hurricane.  Winds are 111-129 mph.");
                break;
            case 4:
                NSLog(@"This is a very large hurricane. Winds are 130-156 mph.");
                break;
            case 5:
                NSLog(@"This is an extremely powerful and dangerous hurricane. Winds are greater than 156 mph.");
                break;
            default:
                NSLog(@"This is not a possible value for a hurricane category.");
                break;
        }
        
    }
    return 0;
}


[3.4] Code snippets (5:15)
--------------------------
Grab a code snippet, indent it to match the indent of your project, then add
comments to it, then select the entire snippet you just modified and save it as
your own code snippet. Time yourself and record how many seconds it takes you to
do all this.

   //If the first condition is satisfied, it will execute this first option.
                if (<#condition#>) {
                    <#statements-if-true#>
                }
                //Otherwise, it will execute the else option.
                
                else {
                    <#statements-if-false#>
                }

2 minutes and 17 seconds. (It took me a minute to find where my code snippet was being cataloged in the library.)


[3.5] Operators and expressions (11:08)
---------------------------------------
List the 6 types of operators described in this video. Provide their name, a
description of their meaning, and the syntax you would use to execute them. What
code snippet does the ternary operator replace?

ARITHMETIC OPERATORS
These include plus +, minus -, multiply *, and divide / and function like their equivalents from mathematics. 

Assigment operator  =
Although it resembles an equal sign =, it does not serve that function. Rather, it assigns a value to a variable. For example:
int hurricane strength = 3

The plus equals operator +=, minus equals operator -=, multiply equals operator, and division equals operator /= takes the current value of a variable and performs the appropriate mathematical operation on it and then sets the variable to that new value. For example:
shieldStrength += 5
This takes the current value of shieldStrength, adds 5 to it, and sets the variable shieldStrength to that new value. 

COMPARISON OPERATORS
== equals
!= not equal
> greater than
< less than
>= greater than or equal to
<+ less than or equal to

LOGICAL AND/OR OPERATORS 
The Logical And && performs an operation only if both conditions are true. For example: 
if (zombies == 0 && vampires == 0) {
NSLog(@“It is okay to open the door”)}
The all clear statement will be printed only if both conditions have been satisfied. 

The Logical Or Operator || performs an operation if either of the conditions are true. For example:

if (rain > 0 || sleet > 0) {
NSLog(@“Bring your umbrella.”)
The notice will be printed if either of the conditions are true. 


MODULUS OPERATOR
The Modulus Operator % performs division on an integer and returns the remainder. For example:
int example = 53 % 5
The result will be the remainder of 53 divided by 5, which is 3. 


INCREMENT/DECREMENT OPERATORS
The Increment Operator a++ takes a variable, adds one to its current value, and assigns the result as its new value.
The Decrement Operator a- - takes a variable, subtracts one from its current value, and assigns the result as its new value.
For example: 
int a = 99;
NSLog(@“There are now %i bottles of beer on the wall.”, a- -);
Here the decrement operator reduces the value of a by one.


TERNARY OPERATOR
The Ternary Operator replaces an if-else statement. Here is an example:

int carSpeed
int speedLimit
BOOL amSpeeding = (carSpeed > speedLimit) ? yes : no ;




[3.6] Loops (8:53)
------------------
Think of a scenario while using a mobile app that might require you to use a
"continue" statement in the middle of a loop.

-The app “Temple Run” seems to follow a loop-like progression on straight-aways. It diverts from this loop briefly for turns and then returns to basic straight-away progression, in the same way that a “continue” statement causes a temporary diversion from a repetitive loop. 


[3.7] Functions (10:16)
-----------------------
What is a function? What is a function prototype? What are the purposes of each?
What are the rules for when and how you can call a function?

-A function is a chunk of code that we set aside and give a name so that we can call it whenever we want. It makes it possible to easily reuse the same code at different times in a program and to feed it different values.
-A function prototype introduces the fact that the program contains a particular function with having to clutter the area above the main function with all of the details of what that function will do. 
-Call the function inside the “main” function on a separate line by writing the name of the function to be called followed by parentheses, which should contain the parameters if any or otherwise may remain empty. The function must be declared before it can be called. However, a function prototype can be used to declare the function early so that it can be called in “main” before its details have been enumerated. 


Section 4: Variables
====================
[4.1] Data types (7:06)
-----------------------
What are the primitive data types in Objective-C? Why did Apple add a set of
classes to handle other data types?

-The primitive data types in Objective-C are int, float, double, char, and BOOL. Apple supplemented these with composite data types to greatly improve the speed and convenience of programming in Objective-C. For example, although it is possible to construct a string using an individual char variable for each letter, it is far more convenient and practical to use Apple’s NSString data type and enter the entire string at once. 


[4.2] Working with numbers (9:33)
---------------------------------
Make a table of Objective-C primitive data types. Add numeric data types and
their properties to this table.

TYPE         |   MEMORY USED           |    STORES    
int          |   4 bytes               |    Integers from -2,147,483,648 to 2,147,483,648                           
unsigned     |   4 bytes               |    Integers from 0 to 4,294,967,295
long         |   4 bytes in 32 bit     |    Integers from -2,147,483,648 to 2,147,483,648
             |   8 bytes in 64 bit     |    Integers from -9223372036854775808 to 9223372036854775808
long long    |   8 bytes               |    Integers from -9223372036854775808 to 9223372036854775808
short        |   2 bytes    	       |    Integers from -32,767 to 32,767
float        |   4 bytes               |    Floating point numbers
double       |   8 bytes               |    Floating point numbers



[4.3] Working with characters (4:39)
------------------------------------
Add char and BOOL (the character data types) to your table created above.

char         |    1 byte               |    One character from the ASCII set. 
BOOL         |                         |    An integer that represents “true” or “false”


[4.4] Variable scope (8:06)
---------------------------
Describe in your own words what the scope of a variable is in Objective-C

<-A variable’s scope is the portion of the program that it can be accessed in.

[4.5] Enumerations (3:35)
-------------------------
What does the `enum` keyword allow you to do?

-“Enum” allows us to define a narrow, custom set of possible values using words, which are easier to recognize as we are writing a program. 

[4.6] Using typedef (2:17)
--------------------------
When would you define your own data type versus using an enum?

-The main advantage of creating one’s own data type seems to be simplifying some subsequent programming. If one made very little use of an “enum” in the program it may not be worth the bother of setting up one’s own data type. However, if it is something that will be used many times over the course of the program, then creating a typedef might streamline the process and save time.

[4.7] Preprocessor directives (5:56)
------------------------------------
Describe the three common preprocessor directives, `#import`, `#define`, and
`#if DEBUG`. Come up with one example where you would use each.

-The preprocessor directive “#import” tells the compiler to find the named code and paste it into the program. This is used on a regular basis, as when we add “#import <Foundation/Foundation.h>” at the top of a program in order to be able to make use of the code contained within that “Foundation” file.
-The preprocessor directive “#define” creates a macro, which is commonly used to create a value and name it. It will then remain constant throughout the program, unlike a variable. In a donut store app, we might set the value of “dozen” at 12, since this will remain constant throughout. It is also convenient to be able to call up existing definitions that have already been loaded into an Objective-C library.
-The preprocessor directive “#if DEBUG” allows us to add notes that will only appear when the program is in debug mode but will not appear when the program is compiled and run.


[4.8] Working with strings (7:52)
---------------------------------
Define the same string using both NSString and C-style string syntax. Describe
the purpose behind each part of your definition.

NSString *message = @“example”;

-“NSString” is the type. It links to code in the foundation framework that allows for the use of strings within Objective-C. The NS comes from the NextStep operating system. 
-The * is a pointer, which means that the variable “message” does not hold the string but rather contains a pointer that leads to another place in the memory where the string is actually stored. 
-The @ indicates that the string within the quotation marks is an NSString.
-The double quotes are necessary, and the content within them is the string. 
-The semicolon is necessary to complete the line.

I am less certain about a C-style string definition, but I think it would be this:
char message[ ] = “example”;




Section 5: Classes
==================
[5.1] Introduction to object orientation (7:36)
-----------------------------------------------
Create an encapsulated (including generalized attributes and behavior)
description of a `MobileMakersParticipant` class. Instantiate a single object
representing yourself as a member of this class.

Yes.	

[5.2] Using objects and pointers (6:38)
---------------------------------------
What is the pointer’s role in instantiating an object from a class? How is a
pointer different than a primitive?

-A pointer is always used in instantiating an object in order to assign the memory that will hold that object and the pointer that will hold that memory’s address. 

-In a primitive data type, the variable holds the object directly. A pointer does not actually hold the object; instead it holds the location of the memory that holds the object. 


[5.3] Messages and methods (6:44)
---------------------------------
What is the main difference between Objective-C’s messages and method calls in
other languages? How can this difference be seen as an advantage while
programming?

-The main difference is that in Objective-C, when one has a method that takes multiple arguments, the method name is split into one piece for each argument.
[myObject: myMethod: “test” partTwo: “test two”];

-The advantage of this approach is that the arguments are then labeled, which makes it much easier to work with them later or for another programmer to come along later and be able to quickly understand exactly what each argument is.


[5.4] Using existing classes in the foundation framework (8:40)
---------------------------------------------------------------
What's the difference between a class method and an instance method?

-An instance method works on an object (which is an instance of the class in question) and thus requires an object in order to be called. 
-A class method is instead called using the name of the class and operates at the class level. 


Try typing "NSD..." into your code window. Use the autofill feature and select a
single class name that starts with those three letters. Once the name has been
auto-completed, use the handy shortcut (Option + click) and investigate the
class whose name just got printed to the screen. Examine the task list for this
class. Do this a few more times until you're familiar with the process, or until
you've exhausted your curiosity, whichever comes last.


Section 6: Memory Management
============================
[6.1] What's new with memory management? (1:45)
-----------------------------------------------
Let it soak in. No questions for this one.

<<PHEW>>

[6.2] Memory management in Objective-C (6:58)
---------------------------------------------
What is the relationship between a pointer to an object, a block of memory, and
the owning and releasing process. Can you come up with an analogy for this
relationship?

-When an object is created, a block of memory is set aside to hold it, and the pointer holds the address of that block of memory. At this time the retain count is set to one. So long as this is the case, the memory continues to hold that object. When the program releases the object, the retain count drops to zero, and Objective-C reclaims that block of memory. 


[6.3] Object creation (7:31)
----------------------------
What does the new method do when used to create an object instance of a class?
Why do we avoid using this method? How long is an object's lifetime?

-The new method allocates a chunk of memory appropriate to the size of the object. Then it goes through and initializes variables internally. Finally, it figures out the address of this portion of memory so that the pointer can then hold that address. 

-For object instantiation in Objective-C, allocation and initialization are usually separated. This is because there are different init methods that can be employed in different situations. Calling the new method takes away those different init options, so calling alloc and init separately is preferred. 


[6.4] Using autorelease pools (5:14)
------------------------------------
How does the autorelease pool work? How and when can you use it deliberately?

-Autorelease pool is a list of objects that need to have release called them. When the pool is drained (at the end of a command-line program or at the end of an event loop in an app), release is called on all of the objects. 

-It is possible to use autorelease anywhere that one would normally call release. However, it is best to use autorelease as little as possible. The example that the lecture provided for when one has to use autorelease is when creating a factory method. 


[6.5] Apple autoreleased objects (3:39)
---------------------------------------
What does ARC stand for? Why is it important to remember this?

-NARC stands for New, Alloc, Retain, and Copy. It is important to remember this because any time one of these is used an object is created and must later be released. 


[6.6] Introduction to Automatic Reference Counting (ARC) (4:43)
---------------------------------------------------------------
What does ARC save us from having to do? How does it keep us from having to make
this extra effort?

-ARC saves us from having to keep track of and release our objects. The compiler adds the release calls for us when it runs so that we don’t have to. 


[6.7] What ARC manages (2:42)
-----------------------------
What are the differences between ARC and garbage collection? What makes these
differences advantageous?

-Garbage collection can slow down programs unexpectedly when it runs because it operates while the program is running. By contrast, ARC is run when the program is compiled so that no changes need to be made when the program is running.  

-ARC is advantageous because it is predictable and because it does not slow down a program’s runtime.


[6.8] The rules of ARC (4:20)
-----------------------------
Why can you not release or dealloc memory when working with ARC?

-One cannot use release or dealloc when working with ARC because releasing is now the responsibility of ARC, and attempting to manually release could create problems. From a more practical standpoint, we cannot call release or dealloc when using ARC because Xcode will call an error and not permit it. 


Section 7: Custom Classes
=========================
[7.1] Creating your own classes (14:01)
---------------------------------------
What are the two different sections used to create a class? What do they hold
and what files are they placed in?

-A class is split into two sections, interface, which is a .h file and implementation, which is a .m file. 

-The .h interface file lists the properties and methods of the class. The .m implementation file actually implements these properties and methods, providing the code that makes them function and do what the implementation promised that they would. Each property is synthesized using two methods, one to set its value and one to get it. 

    
**Challenge!** Create a Tweet class for a twitter style app.


I would probably have many classes in a Twitter app: Timelines, Notifications, Messages, Profile . . . 

So I tweet class would likely be responsible for the act of posting a tweet. Its properties would include the name and twitter handle of the person posting the tweet. Its methods would include providing a window to type in, spell check, and post.

So the .h interface file might look like this:

#import <Foundation/Foundation.h>

@interface Twitter : NSObject

@property NSSTring *username;
@property NSString *twitterhandle;

-(void) provideWindow;
-(void) type;
-(void) spellCheck;
-(void) post;

@end


And the .m implementation file might look like this:

#import "Twitter.h"

@implementation Twitter

@synthesize username;
@synthesize twitterhandle;

-(void) provideWindow { some code   }
-(void) type { some code   }
-(void) spellCheck { some code   }
-(void) post { some code   }

@end


[7.2] Defining methods (8:36)
-----------------------------
**Challenge!** Define what should get passed in and what should get returned by
each of your methods in your Tweet class above.

I’m not sure how to create a provideWindow method. (I had in mind providing the little window in which to type the tweet.) Perhaps that should have been a separate class. In any case, it is beyond my current knowledge base. I think that the rest of the methods would each take and return an NSString, and they could be constructed consecutively so that the result of the first method is the input of the second one and so on:  

-(NSString *) type: (NSString *) input;
-(NSString *) spellCheck: (NSString *) type;
-(NSString *) post: (NSString *) spellCheck;

<<DO YOU LIKE TWITTER?>> 
	I feel like maybe I should. And I've tried it. But I got bored with it and had more important things to attend to. 

[7.3] Defining properties (7:21)
--------------------------------
How did Objective-C programmers handle instance variables before 2012? How are
they handled now? What got easier and what got obscured?

Previously there were no properties in Objective-C. Instead, one defined all of the instance variables at the top of the header (.h) file inside a set of curly braces. It was then necessary to write a getter and setter method for each instance variable. 

It is still possible to do this. However, now it is preferable to use “@property,” which takes care of the getter and setter and makes declaring the instance variable unnecessary. One can still use instance variables; the best practice is to just include them at the top of the implementation file in curly braces. 

It is also no longer necessary to add the “@synthesize” at the top of the .m file for every property in the .h file. Now, declaring the property in the .h file results in the compiler automatically generating the instance variable with the leading underscore along with the getter and setter methods. 

This automation makes the job of the programmer easier. However, the work still takes place behind the scenes by the compiler. 


[7.4] Defining initializers (12:30)
-----------------------------------
What are initializers and why do we need to use them? Describe a situations when
you can rely on the standard `init` method and when you have to create your own
custom initializer.

-Initializers make sure that when the class being initialized is used to create new objects their internal variables will have meaningful values. 

-The standard init method is appropriate when the initial values of one’s variables are not important or when they should begin at zero. In a banking app, for example, the classes representing accounts should begin at zero until deposits are added to change that state. 

-A custom initializer is appropriate when we want the class to initialize new objects with some existing value. For example, in a clock app, we might have a class in which new objects should be initialized with a value for the current time. 


[7.5] Using dealloc (5:33)
--------------------------
Why can we have a dealloc method in a class when using ARC, but we can't call
dealloc manually oursevles when using ARC?

-One can write a dealloc method to release some resource like a database that wouldn’t otherwise be released. However, we cannot call it manually; Objective-C runtime runs the dealloc method when it is appropriate so that we don’t have to worry about it. 


Section 8: Collections
======================
[8.1] Working with C-style arrays (7:12)
----------------------------------------
What are the three constraints when using C-style arrays? Create a C-style array
that holds the days of the week.

1. There is no bounds checking. 
2. They have a fixed size.
3. One cannot mix different types of data within a C-style array.

NSString *daysOfTheWeek[7] = {@“Monday”, @“Tuesday”, @“Wednesday”, @“Thursday”, @“Friday”, @“Saturday”, @“Sunday”}


[8.2] Working with Objective-C array objects (8:00)
---------------------------------------------------
What is the difference between a mutable and an immutable array?

-A mutable array contains additional methods that allow us to change the contents of the array by either adding to it or removing an item from it. 


**Challenge!**
Create an immutable array containing the days of the week. Create a mutable
array that contains the days of the week that you will be at Mobile Makers. Add
the days of the week from the immutable array to the mutable array.

NSArray *daysOfTheWeek = [[NSArray alloc]initWithObjects:@“Monday”, @“Tuesday”, @“Wednesday”, @“Thursday”, @“Friday”, @“Saturday”, @“Sunday”, nil];

NSMutableArray *daysOfMobileMakersAcademy = [[NSMutableArray alloc]initWithObjects:@“Monday”, @“Tuesday”, @“Wednesday”, @“Thursday”, @“Friday”, nil];

[daysOfMobileMakersAcademy addObject:daysOfTheWeek];


[8.3] Using dictionaries (5:55)
-------------------------------
Create a dictionary that lists five or more events in your life and the
accompanying year (or date if you want to get fancy) of the event.

NSDictionary *lifeEvent = [[NSDictionary alloc]
initWithObjectsAndKeys: @“Birth”, 1971,
@“Marriage”, 1996,
@“Son born”, 1998,
@“Daughter born”, 1999,
@“Mobile Makers Academy”, 2014, 
nil];


[8.4] Fast enumeration (3:27)
-----------------------------
Use fast enumeration to log the timeline of the life events you described above
to the console.

NSDictionary *lifeEvent = [[NSDictionary alloc]
initWithObjectsAndKeys: @“Birth”, 1971,
@“Marriage”, 1996,
@“Son born”, 1998,
@“Daughter born”, 1999,
@“Mobile Makers Academy”, 2014, 
nil];

for (NSString *event in lifeEvent) {
NSLog(@“One life event is %@.”, event};


Section 9: File Management
==========================
[9.1] Introduction to file management in Objective-C (6:44)
-----------------------------------------------------------
What can you do with files using the methods you are aware of that are available
in Objective C’s Foundation class?

-We can move a file, copy it, get its attributes, remove it file, or simply check to see if it exists. 


[9.2] Working with paths and URLs (7:17)
----------------------------------------
What are the three parts of a URL? What are the advantages to using NSURL?

-The scheme, the domain, and the path.

-NSURLs are faster, they have better error protection, and they are used in newer and more powerful classes.


[9.3] Reading and writing strings (4:38)
----------------------------------------
What would be a reason you would want to write a string to disk instead of just
keeping it memory?

-A big advantage of writing a string to the disk is permanence. The information can then be available to the app or user later and can survive the app or even the device being shut down. 


[9.4] Archiving objects (12:41)
-------------------------------
Why would you want to archive an object instead of writing the data to disk
using the techniques discussed previously?

-An object that contains multiple pieces of data of different types would require a great deal of work to break down into its component parts and write each to the disk separately. Archiving it automates that process. The archived version also seems to be better organized and easier to work with, which may help avoid errors. 


Section 10 - More Complex Classes
=================================
[10.1] Inheritance and NSObject (8:13)
--------------------------------------
How can you determine what methods you're inheriting from a super class? How do
you overide a method inherited from a super class?

-To determine which methods are being inherited from a super class, we can check its documentation by using click and option on the super class and then opening its class reference. 

-In Objective-C one can override a method by creating a new method with the same signature in the .m implementation file. 


[10.2] Extending classes with categories (6:31)
-----------------------------------------------
What is the difference between a category and an inheritance? What are the
limitations of using a category?

-Inheritance creates a new subclass based on the superclass that it is inheriting from. Category, by contrast, simply adds new methods to an existing class. The limitations of using a category include the inability to add instance variables or properties. 


[10.3] Defining protocols (5:14)
--------------------------------
How are protocols useful?

-They standardize interaction between objects without having to use inheritance. An object just has to conform to all of the mandatory (as opposed to the optional) protocols. 


[10.4] Dynamic typing (11:33)
-----------------------------
What are the advantages and disadvantages to dynamic typing?

-Dynamic typing is advantageous for circumstances in which the type of the objects in question is mixed or not known. However, static typing is preferable where possible because it puts more checking into the compile stage.


