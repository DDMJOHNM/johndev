---
title: "The Solid Principles Of OOP Design"
date: 2022-10-18T16:56:59+13:00
draft: true
---


## Single Responsibility Principle (SRP)

A class should only have one and only one reason to change.



## Open-Closed Principle


Objects or entities should be open for extension but closed for modification.

This means that a class should be extendable without modifying the class itself.



## Liskov Substitution Principle


Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

This means that every subclass or derived class should be substitutable for their base or parent class.



## Interface Segregation Principle (isp)


A client should never be forced to implement an interface that it doesnt use, or clients

should not be forced to depend on methods they do not use.




## Dependancy Inversion Principle (Dip)


Entities must depend on abstractions and not concretions. It states the high level module must not depend on the low-level module they should depened on abstractions

This principle allows for decoupling


https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design#interface-segregation-principle