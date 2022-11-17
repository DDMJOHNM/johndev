---
title: "Modules In EzyVet"
date: 2022-10-18T16:56:59+13:00
draft: false
---

## Data Transfer Objects 
- Used for storing data and passing data between systems

## Entities 
- Represents a piece of a data that can be stored in the database 

## Request -> DTO Mapping 

- As soon as a request is received for a post or a patch request it will be validated
using the Laravel request validation  

## Service Providers and Contextual Binding 

Service Provider Bootstraps application
Registers Dependancies and binds them to the Service Container 
Depenedancy meets contextual restrictions 
and it will try to create an instance of that dependency And inject it into the class 