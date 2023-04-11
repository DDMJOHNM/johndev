---
title: "Hands On Arcitecture"
date: 2023-04-06T16:56:59+13:00
draft: false
---

# Hands on Architecture 

## Role Of the Architect
- Define a blueprint

## Requirements Clarification 
- Top level functional and non functional requirements (system qualities)  

## True North   
- Engineering Principles for the system
- High level design (Decomposition of system into components)
- Quality Attributes 
- Product Velocity (cicd)
- a/b testing - every feature has a flag 

## Technology Selection 

## Leadership 
(Steering and asking tough questions at design meetings)

## Coaching and Mentoring Developers 
- Outside of their normal deliverables

## Target State vs Current State
- mvp 
- next bite sized chunks after that 

## Software 

## Architecture vs Design 
- High Level Structure 
- Low Level Implementatiion Details 

## What does Architecture look like?
- High Cohesion (Component Performs Single Task)
- Low Coupling (low dependancy between themselves) 
(Component can be extended or completely replaceable)

### See Robert Martin Concentric Circles
- Enterprise Business Rules
- Application Business Rules
- Inteface Adapters
- Frameworks and Drivers 

Different Architectures will bring out different numbers and sets of circles.

## Main Architectural Paradigms that are commonly used.

- Package Based
- Layering/N-tier/3-tier
- Async / message-bus / actor model / Communicating Sequential Processes(CSP)
- Object Oriented
- MVC/Separated Presentation
- Microservices/Service Oriented Architecture (SOA)

## Microservices 

A simple standalone application 

Three distinct layers:
- Front end 
- Back End 
- Data Store

As product features start to multiply 
- Code complexity increases 
- Operational work increases (Dev Ops)
- Product Hits Scalability Limits
- Developers write huge amount of tests as quality gates

Applications in this state are called 'Monoliths' 

Each microservice is autonomous, self contained and individually deployable and scalable.

Each Feature can be a microservice.

## Challenges for Microservices

- Efficientcy.
- Programming complexity. (Compartmentalisation key to managing)  
- Synchronisation Primatives - mutexes and Semaphores (Deadlocks)
- Priority Inversion - High priority process wait on Low Priority Process
- Starvation 


## Golang to solve these challenges

- Code becomes hard to read and poorly documented. 

- Contracts between components cannot be easily inferred.

- Builds are slow. The development cycles of code-compile-test grow in difficulty,with inefficiency in modeling concurrent systems, as writing efficient code with synchronization primitives is tough.

- Manual memory management often leads to bugs.

- There are uncontrolled dependencies.

- There is a variety of programming styles due to multiple ways of doing
something, leading to difficulty in code reviews, among other things.


## Concurrency

With shared memory its easy to get deadlocks or corruption if a process crashes or misbehaves.

CSP promotes messaging using channels queues with a logical inteface of send() and recv()   

First class channels. (First Class Go Primatives)
Proceedures called go routines.

## Garbage Collection 
In a concurrent system garbage collection is a must have feature 

## Object Orientation

Go way is composition over inheritance
For Polymorphic Behavior Go uses interfaces and duck typing.  