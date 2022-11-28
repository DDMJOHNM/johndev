---
title: "Design Patterns"
date: 2022-10-18T16:56:59+13:00
draft: true
---

## Keeping your objects in the know 
take the parts that vary and encapsulate them 
so you can later alter or extend the part that vary without 
affecting those that dont.

eg duck class with flying and quacking interfaces.

Polmorphic types
abstract class animal 
two concrete implementations do and cat.

assign cmncerete implementation object at run time.
Animal animal = new Dog()
animal .makeSound();

a = getAnimal();
a.makeSound();

duck class
Intefaces fly and quck behavior -

add new behaviors without touching any of the duck classes that use flying behaviors 
duck now delegates flying and quacking behavior.

add instance variables (interfaces) we instanciate the behavior class
delegate interface behavior to the the behavior class 

```

public class MiniDuckSimulator {
    public static void method main(Stirng[], args){
        Duck mallard = new MallardDuck();
        mallard.performQuck();
        mallerd.performFly();

    } 
}

calls mallard duck inherited performQuck method which then delegates
to the objects quak behavior ie calls quack on the ducks inherited quack beahvior reference  

set and get behavior on duck subclass ratgher than inheriting through the duck constructor
call these methods anytiime you want to chnage the behavior 

Duck model = new ModeklDuck();

model.setFlyBehavior(new FlyRocketPowered());

encapsulated behaviors
is a and has a and implements
each set of behaviors as an encapsulated family of alogrithms

the has a relationship each duck has a fly beavior and quack behavuior to which it dlegates flying and quacking
composition instead of inheriting their behavior ducks get their behavior form being composde of the right objects.

FAVOUR COMPOSITION OVER INHERITANCE

Strategy Design Pattern 
defines a family of algoritms, encapuslates each one, and makes them integchangeable
Strategy letes algorithms vay independently from the cleints that use it. 


```









