# 🧱 SOLID Principles: The "Raw" Plain English Guide

*Module can be anything -> function, file, class. In system design, we use modules to simplify the general form of an application. Context matters a lot.*

Here is my raw, no-nonsense breakdown of the SOLID principles.

## 1. Single Responsibility Principle (SRP)
SRP is just a rule that keeps classes small enough to be mentally manageable by **only one person/role**. That's the whole thing. It's a law designed to make developer life easier to code and navigate.

> **The Rule:** No one must care how a class is implemented except the single person handling it. Others using it can simply request that single handler to add functionality.

**Real-world approach:** If the Email team wants something from the DB, they ask the DB team. The DB team figures out changes via a SyncUp, updates the Low-Level Design (LLD), and assigns the new classes to people. This skyrockets the value of **ownership** ("This is my class, and I am responsible for its performance").

## 2. Open/Closed Principle (OCP)
The entire principle boils down to one question:
**"Can I add new functionality or methods without touching previous code?"**

## 3. Liskov Substitution Principle (LSP)
If you are inheriting methods, those method signatures are fixed and you cannot change them. 

However, one can override the internal working according to the inherited class workspace. 
*Note: Interface in a class MEANS the method (since via abstraction, what we see is the interface—i.e., variables and method names—and not their functioning).*

## 4. Interface Segregation Principle (ISP)
If even one object of my class can't use a method or variable because it is not relevant to it, I must drop it and find a fix. 
In short: **Drop irrelevant interfaces.** *(Refresher: Interface means what we see after abstraction and encapsulation are applied).*

## 5. Dependency Inversion Principle (DIP)
I like to call this the **Plug and Play Model**. Thanks to DIP!

Both the high-level switch and the low-level bulb now point to the interface. The dependency has been inverted. 
**What does "inverted" actually mean here?**
It means we are building a wrapper. The high-level component uses the wrapper. We make a different module that has this same abstraction. Now, if we want to change the internal tool choice tomorrow, we can easily do so without breaking the system.

**The Workflow:**
1. Do high-level planning first.
2. Build the APIs according to its requirements.
3. Leverage and mold the low-level tech to fit into the interface. 
*(Not the old way where we see what pipes the code provides and then write high-level code according to it).*

Since control inverts from top to bottom -> **It's inversion.**


By - Aditya Chauhan