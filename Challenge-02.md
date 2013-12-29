From the Lynda.com video series “Foundations of Programming: Object-Oriented
Design”, watch each (short) video and answer the correlating questions:


Section 0: Introduction
=======================
[0.1] What to expect from this course (3:06)
--------------------------------------------
What is the intended purpose and potential advantage of learning object oriented
design?

It gives the user a professional vocabulary, which provides greater clarity and understanding in designing and communicating one’s code. In contrast to earlier forms of programming that were constructed in a more straightforward linear fashion and grew unwieldy as the programs lengthened, object-oriented design breaks a program up into a collection of smaller, interacting mini-programs that contain their own data and logic. This compartmentalized design is far easier to manage. It also simplifies troubleshooting because problems can often be isolated within a single object.


[0.2] Exploring object-oriented analysis, design, and development (1:41)
------------------------------------------------------------------------
Why might it be advantageous to analyze and design before beginning programming?

Beginning to build a program without analysis and design would be like attempting to build a house by grabbing some wood and nails and starting to hammer them together without a plan. You might get the job done eventually, but you will have far more success and a much easier journey if you first analyze the problem and then design a well thought-out approach before beginning to build a house or a program. 


[0.3] Reviewing software development methodologies (4:08)
---------------------------------------------------------
What is the difference between a "waterfall" and an "agile" approach to
development? What is an iteration and how do we to use them to build software?

In a waterfall approach, creating a program is done in a strictly linear series of steps. Each step is fully completed before moving on to the next, and the movement through the steps is only forward without any backtracking. 
An agile approach moves through all of the steps quickly creating an initial draft of the program. Based on what has been learned in this process, a new analysis is made, improvements are designed, and another iteration is built. This may be repeated many times. 
An iteration is a draft or version of the program. Quickly creating an initial iteration makes it possible to test the concept and design in practice, perhaps get early feedback from a client, and learn from this to improve successive iterations. In this way, the program evolves through a series of gradually improving iterations. 


Section 1: Core Concepts
========================
[1.1] Why we use object-orientation (2:42)
------------------------------------------
What are the various types of programming languages and in which domain is each
used?

Procedural languages like Fortran and Cobal have largely been eclipsed by object-oriented programming languages. Logic programming languages like Prolog and functional programming languages like Haskell are used in academia and for highly specialized purposes. Most of the languages developed in the last 30 years have been object-oriented. And most consumer-oriented programming for gaming, mobile apps, desktop apps, and web apps use object-oriented programming languages. 


[1.2] What is an object? (5:22)
-------------------------------
Describe in your own words the three properties of a computing object.

An object’s identity is what sets it apart as unique from other objects. An object’s attributes are the characteristics that describe it. And its behavior consists of the actions that it performs. 


[1.3] What is a class? (4:43)
-----------------------------
Explain how classes are analogous to blueprints. Include the relationship
between a class and an object. Can you think of how the analogy breaks down?

In the same way that a blueprint provides the instructions to make a house and can be used to make multiple houses after the same pattern, so a class can be used to make a number of different objects, each of which is an instance of that class. However, a class differs from a typical blueprint in that it contains a number of attributes which are blank and can be filled in differently for various objects that serve as instances of that class. 


[1.4] What is abstraction? (2:45)
---------------------------------
When a developer uses the term “abstraction” what are they describing?

In the process of abstraction, a developer focuses on only the essential qualities of the concept for which they are creating a class and deliberately ignores and excludes all unimportant details. 


[1.5] What is encapsulation? (3:45)
-----------------------------------
What does encapsulation prevent? What does it enable?

Encapsulation protects the attributes of the class and its objects so that they cannot be changed from outside except through appropriate behaviors that have been designed to affect these attributes. It makes it possible to change the inner workings of one class without affecting the rest of the application. 

[1.6] What is inheritance? (3:35)
---------------------------------
Describe the inheritance relationship between classes. When would this
relationship be advantageous to establish?

-When a programmer needs to create a new class that includes all of the attributes and behaviors of an existing class plus one on more additions, they can use the existing class as a superclass and create a subclass that inherits all of its attributes and behaviors. This makes creating the new class far easier as the programmer now only needs to add the necessary additions to the subclass. 
-This would be advantageous in any circumstance in which a new class is needed that includes the attributes and behaviors of an existing class. In these situations making use of inheritance will save the programmer time and labor.  

[1.7] What is polymorphism? (3:22)
----------------------------------
What is the basic idea behind polymorphism? How can it make the classes we
create more flexible?

-Polymorphism means that the program will automatically do the correct behavior based on the situation at hand, even if there are multiple possible behaviors. To borrow one of their examples, a program will add when a “plus” sign is between two integers but concatenate when it is between two strings. 

-We can override a method from a superclass in one or more of its subclasses. In this way the same method can be customized for the different requirements of each subclass. This allows the subclasses to be flexibly tailored to fit the requirements of the program’s design. 


Section 2: Object-Oriented Analysis and Design
==============================================
[2.1] Understanding the object-oriented analysis and design processes (4:13)
----------------------------------------------------------------------------
What are the steps of analysis that come before writing code for an application?
Why do you think these steps make writing the code easier?

Gather requirements
Describe the app
Identify the main objects
Describe the interactions
Create a class diagram

They provide a well-thought out and carefully organized plan of attack, which will spare the programmer a great deal of time and labor relative to a less organized, more haphazard approach. By first figuring things out on paper, the programmer knows which classes will be needed and how they will need to interact and has a good sense of how the entire program will operate before ever writing a line of code. 

[2.2] Defining requirements (6:09)
----------------------------------
What should you have after you've completed the first phase of defining your
requirements?

After the first phase of defining requirements, one should have a written list of the bare minimum requirements that the program must meet. 


[2.3] Introduction to the Unified Modeling Language (UML) (1:54)
----------------------------------------------------------------
What is UML? Why Is it useful to visualize your application before coding it?

-UML or Unified Modeling Language is a system of graphical notation used to create a visual representation of an object-oriented system. 
-It helps the programmer(s) understand what the program needs to do and how it needs to be organized. This makes it possible to know in advance what coding will need to be done and how the different parts (objects and classes) of the program will need to be structured and how they will interact with each other. 

Section 3: Utilizing Use Cases
==============================
[3.1] Understanding use cases (6:11)
------------------------------------
Write a use case for creating an event on your phone's calendar.

Title: Create an event on iPhone calendar
Actor: iPhone user
Scenario:
1. User opens the calendar
2. User selects a date on the calendar
3. User chooses to add an event to that date
4. A form opens with places for the user to enter the title of the event, its location, its start and stop times, and any additional notes that they desire to add. 
5. Additional options are offered, including the ability to designate the event as taking up the entire day, to create an alert, to tag the entry with a keyword, to repeat the event, or to invite others. 
6. When the user has finished adding as much detail as they desire to the entry, they press “done” to confirm that it is complete. 
7. The user is then shown their completed event entry. 


[3.2] Identifying the actors (4:16)
-----------------------------------
Can you think of a use case for a mobile application in which the actor is not
the user of the mobile device?


Title: Wireless speakers play music
Actor: Wireless speakers
Scenario:
1. Wireless speakers alert Music app (or other audio application) of their presence via bluetooth
2. Music app recognizes speakers. 
3. If audio is currently playing, the computer streams the content to the speakers via bluetooth. 
4. If the speakers shut off or become out of range, the program stops streaming the audio to them and switches back to the built-in speaker. 



[3.3] Identifying the scenarios (5:07)
--------------------------------------
Write another use case for a mobile device user interacting with a calendar
application. This time include a couple extensions when crafting your scenario.


Title: Create an event on iPhone calendar
Actor: iPhone user
Scenario:
1. User opens the calendar
2. User selects a date on the calendar
3. User chooses to add an event to that date
4. A form opens with places for the user to enter the title of the event, its location, its start and stop times, and any additional notes. 
5. Additional options are offered, including the ability to designate the event as taking up the entire day, to create an alert, to tag the entry with a keyword, to repeat the event, or to invite others. 
6. When the user has finished adding as much detail as they desire to the entry, they press “done” to confirm that it is complete. 
7. The user is then shown their completed event entry.

Extensions:
The user has failed to enter any information in the form before clicking “done.”
a. Create an event at that time with the generic label “new event.”

There is already an event at that same day and time. 
a. Split the entry for that time slot horizontally in order to accommodate two or more additional entries
b. Place the old entry in the first new space.
c. Place the new entry (or entries) in subsequent spaces.



[3.4] Diagramming use cases (4:18)
----------------------------------
Do a google image search for "use case diagram." Notice how many variations
there are. What do they all generally have in common?

One or more users are shows as stick figures.
One or more user case titles are shown surrounded by ellipses.
Lines run between users and the use cases that they will interact with. 


[3.5] Employing user stories (3:43)
-----------------------------------
Write 5 user stories to describe a mobile user interacting with his or her maps
application.

As a commuter
I want to know the length of time that my commute will take
So that I can know when to leave in order to arrive on time

As a traveler
I want to know the fastest route to my destination
So that I can safely and quickly drive there

As a shopper
I want to know the location of a particular business
So that I can shop there

As a jogger
I want to know the length of a particular route
So that I can keep track of how far I have run

As a user of public transportation
I want to know the bus or train that I need to take to most quickly reach my destination
So that I can arrive there in the least amount of time


Section 4: Domain Modeling (Modeling the App)
=============================================
[4.1] Creating a conceptual model (1:59)
----------------------------------------
What’s your favorite color?

Red


[4.2] Identifying the classes (2:27)
------------------------------------
Identify the classes in the use case you constructed for a user interacting with
his or her calendar application in chapter 3.


User 
Calendar
Date 
Event 
Form 
Timer
Alert
Keyword
Repeat
Invite
Generic label
Split



[4.3] Identifying class relationships (2:38)
--------------------------------------------
Identify the relationships among the classes you found above. Create a
conceptual model where you diagram these relationships and then upload a picture
of your model below.

I created a file called "ClassRelastionships.png" and attempted to git add it.

[4.4] Identifying class responsibilities (6:43)
-----------------------------------------------
Identify the responsibilities of the classes you found above. List them here.

Class: Add
Responsibility: Opens form to add new event

Class: Form
Gets details including title, location, repeat, invite, alert. 
Links to Timer class

Class: Alert
Provides notification of event

Class: Timer
Sets start and stop times for event.

Class: Date
Provide Add option to create new event
Displays new and existing events



[4.5] Using CRC cards (2:49)
----------------------------
If you’d like, try creating CRC cards for the model you made above. There's no
need to respond here, just try it out and see if you like this form of
organization.



Section 5: Creating Classes
===========================
[5.1] Creating class diagrams (6:11)
------------------------------------
Construct Class Diagrams for the classes you imagine exist in a twitter app, a
maps app, a calendar app, or any other app you would like to make. Do you find
that it is easier to come up with the attributes or with the behaviors? Why do
you think that is?

Map
Use Case Scenario:
	User types in an address. Map verifies that it is a real address and displays its location. User selects it and options appear: “directions to” or “directions from.” Selecting directions then results in the route being shown on the map. Selecting start begins turn by turn directions, which display the actions that the driver must take to reach the destination. GPS tracks the driver’s current location.  

Class: Address

Attributes:
streetAddress: String
city: String
state: String
country: String

Operations:
verifyLegitimateAddress: Boolean


Class: Directions
Attributes: 
toOrFromDestination:

Operations:
getAddress
plotRoute
displayRoute 


Class:
TurnByTurn

Attributes:


Operations:
getDirections
getLocation
displayInstructions
displayNavigation


Class: GPS

Attributes:
isActive: Boolean

Operations:
getLocation
displayLocation


I seem to be having a more difficult time coming up with attributes. The behaviors are easier because they are just what that class does. 


[5.2] Converting class diagrams to code (4:57)
----------------------------------------------
How might the separation of interface and implementation in Objective-C be an
advantage when working with class diagrams?

-The separation of interface and implementation is advantageous because they translate easily from the parts of the class diagrams. The attributes constitute the parts of the interface, while the behaviors make up the implementation.


[5.3] Exploring object lifetime (5:55)
--------------------------------------
What are the constructors and destructors in Objective-C? Why do we use them?

-A constructor is created in Objective-C by creating an “init” method within a class. This makes it possible to assign values to objects when they are first instantiated from that class. A destructor is piece of code that is automatically called when an object is destroyed. In Objective-C this is “dealloc.” A destructor is often used to preserve some data that the object is holding, such as an open document. 


[5.4] Using static or shared members (5:22)
-------------------------------------------
Like the interest rate example in the video, give three additional examples of
data that would be the same for all instances of a class.


-In the clock app, “Alarm” could be a class with multiple instances for one’s different alarms. Yet the current time would be a variable that would be the same across all of the instances. 
-In the map app, “Directions” could be a class with instances for “to,” “from,” and “transit,” but current location would a variable that would be the same for all instances. 
-In a social media app like Facebook, each profiles could be an instance of a class. 
-In a store app, the tax rate could be a constant percentage across all instances of the class “Product.”   



Section 6: Inheritance and Composition
======================================
6.1 Identifying inheritance situations (6:49)
---------------------------------------------
Describe in your own words what inheritance is and how it is useful when
constructing classes.

-In inheritance one class is an example or a kind of another class. This sub- or child-class thus takes (or inherits) the attributes and behaviors of the super- or parent-class. This is useful because it simplifies the coding required. Instead of reinventing the wheel for each related class, recognizing the patterns and relationships among the classes makes it possible to use inheritance to save work and time. 

[6.2] Using inheritance (2:43)
------------------------------
Referring to the apps on your phone, come up with three examples where you
believe methods are being inherited from superclasses and called by subclasses.


-In the mail app, the Inbox, Outbox, Drafts, Sent, Junk, and Trash folders could be subclasses inheriting methods from a Folders superclass. 

-In the lynda.com app, the various courses could be subclasses inheriting methods from a Course superclass. 

-In Candy Crush (which my daughter put on my phone), the different kinds of candies could be subclasses of a Candy superclass. 


