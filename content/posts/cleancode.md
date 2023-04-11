---
title: "Clean Code"
date: 2022-10-18T16:56:59+13:00
draft: true
---

# Chapter 11 Systems

Stay clean at higher levels of abstraction
Seperatioon of concerns
Construction logic mixed in with runtime logic 
Main 
- Abstract Factory Patterm
Dependancy Injection 
Responsibility Passed to an Authoritive Mechanism.
During construction process DI Container Instanciates required objects
Test driven development, refactoring and clean code that is produced make iterations to the systems (tomorrows stories)
work at code level.   
Software Systems can grow incrementallly if the proper separation of concerns is maintained.
Aspect Orientated Programming 
Java Proxies 
Pure Java AOP FrameWorks
AspectJ 
Start with Naively simple but decoupled structure.

```
An optimal system architecture consists of modularized domains of concern, each of which is implemented with Plain Old Java (or other) Objects. The different domains are integrated together with minimally invasive Aspects or Aspect-like tools. This architecture can be test-driven, just like the code.
```
Optimise Decision Making leave late as to be most informed (JIT Decisions)

```
Standards make it easier to reuse ideas and components, recruit people with relevant experience, encapsulate good ideas, and wire components together. However, the process of creating standards can sometimes take too long for industry to wait, and some standards lose touch with the real needs of the adopters they are intended to serve.
```
Systems need domain specific Languages 

```
A good DSL minimizes the “communication gap” between a domain concept and the code that implements
```

Domain-Specific Languages allow all levels of abstraction and all domains in the application to be expressed as POJOs, from high-level policy to low-level details.

```
Systems must be clean too. An invasive architecture overwhelms the domain logic and impacts agility. When the domain logic is obscured, quality suffers because bugs find it easier to hide and stories become harder to implement. If agility is compromised, productivity suffers and the benefits of TDD are lost.
```
Design systems or modules use the the simplilest thing that can possibly work.





