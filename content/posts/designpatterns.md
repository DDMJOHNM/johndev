---
title: "Design Patterns"
date: 2022-10-18T16:56:59+13:00
draft: true
---

Load your brain with design patterns and then recognise them in your designs and 
existing applications where you can apply them instead of code reuse you get experience resuse.

Disadvantages of using inheritance to provide the duck behavior 
-Runtimne changes are differcult to make 
-Changes can effect other ducks 

Inheritance for the purpose of reuse has not turned out so well for maintainance.

-One constant in software design is change 

Design Principles 
Identify aspects of your application that vary and seperate them from what stays the same.
Encapulsation - this will give fewer unintended consequences from code changes.

All patterns provide a way to let some part of the system vary independendently from all the rest.

Duck class (Pull out what varies)
Duck subclass will use a behavior represented by an inteface.  
Flying Behaviors
Quacking Behaviors 
(Duck Behaviors) 
include behavior setters to chnage the behavior of the duck dynamically. (At runtime)

Implementation 

```
inteface flybehavior 
fly()

class flyWithWings
fly(){//implements duck flying}

class FlyNoWay
fly(){//do nothing cant fly} 

all flying classes implement flybehavior interface 
all new flying classes just need to implement the fly method.

interface QuckBehavior
quack()

class Quack
quack(){implenments duck quacking}

class Squeek 
quack(){//rubber duck squeek}

class MuteQuack
quack(){//do nothing can't quack}


```
All objects can reuse fly and quack behaviors as they are no longer hidden away in the duck classes.
Add new behaviors without modifying and of the existing behavior or touching any of the duck clsses that use flying behviors.

Duck now delegates its flying and Quacking behavior.

```

Duck 
FlyBehavior flyBehavior (instance variable)
QuackBehavior quackBehavior  

performQuack()
swim()
display()
performFly()

public class Duck {
    QuackBehavior quackBehavior; 

    public void performQuack(){
        quackBehavior.quack(); 
    } 


} 

We don't care what kind of object it is we just care if it can quack.

```

Look at how the fly and quack variables are set.

page 16 

```


```













