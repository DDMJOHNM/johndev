---
title: "Kafka"
date: 2022-11-13T16:56:59+13:00
draft: false
---

# Journey to Event Driven Programming 

Neil Avery Blog
Karl Waegner

api to event driven architecture
Event Atomic 
Relates to strean of events
Have behavior in ecosystem


Consideration In Event Driven Design 

Domain Driven Design

never overwrite old data -> create current state

Transactionality 
-> data hygene 
-> data validation
-> dead letter queue (Schema Registry) db table insert fail 
-> data model 

Exceution


Security


Lineage
Data Evolves Data will change 
Data Model In Db and get from git. 
Molithic v Distributed


Source


Making the transition 
Observable
Trusted/Transactional/Scalable
Stateless, Cleansing, Enrichment
Stateful
TPS
Error Handling
Dead Letter Queue
Metadata
Data Lineage 

Store 7-14 then into S3
Kafka connect dump into store 
Birth to the Death of the event
Volatility of Data 

Event First Pattern
Distributed to everyone cares about
Micro Service 
Sharding data and copy across brokers
Replicate data accross nodes

Costs of Events First
data Traceability (Meta Data)
Failure paths
Scaling
Lineage
versioning
Auditing
Scaling 

Decoupling
Encaouslating
inverted knowledge
Evolutionary change
event sourcing 

Request Response -> Event Driven

Published -> Topic -> Consumer (See things as they occur)
Schema Registry -> Validation _.next person has resposibilty to react to it 
(Sagas)(Immutable)
Topic with different retention 
kafka complementary to db
db good for reporting 

