---
layout: post
title:  "Spring JPA - 1"
date:   2019-06-19 12:00:00 +0900
comments: true
categories: Spring
---



In this posting, I will write about 
1. ORM paradigm inconsistency problem
2. Basic settings for getting started with Spring JPA

1. ORM paradigm inconsistency problem (disagreement between objects and Relational Database)
It may look easy when thinking about mapping an object directly into a database, but there are many obstacles lying ahead.
    1) Granularity
    -Objects can be made with varying sizes and containg various member variables; they can be cusomized at programmer's will.
    -RDB(Relational Database) has a set of tables with fixed sizes and columns(to begin with) and only primitive data types are allowed as input.

    2) Subtype
    -Objects can have inheritance and polymorphism structures implemented. 
    -RDB has no such thing and there is no way of implementing those concepts

    3) Identity
    -Objects can be checeked for reference equality and instance equality.
    -RDB's primary key corresponds to this.

    4) Association
    -Objects can be referenced by other objects or reference other objects; the direction exists and the arrows can be many-to-many.
    -RDB has foreign key without direction. It needs linking table to express relationships among many tables.

    5) Data Navigation
    -Objects can be navigated through referencing other objects and can iterate collections.
    -RDB is very inefficient in navigating through data, using a lot of time and resources in executing simple iterations.

2. Basic Settings for JPA
Springboot application
application.properties
All JPA should take place in one transaction.

How to?
Domain Model --> Table mapping

1) Annotation (recommended and easier)
@Entity(users) to avoid innate given name in postgres
Generated Strategy is different for various databases
spring.jpa.hibernate.ddl-auto=create <- cr
eates new data everytime application is run

spring.jpa.properties.hibernate.format_sql=true
spring.jpa.show-sql=true

2) Xml

Value type = subordinate to entity (object in objecty)
composite data type = @Embeddalbe @Embedded

One to many relation
many to one relation
How to connect?

Entity status and cascade
- Using cascade option (@OneToMany(cascade = cascadeType.Persist etc...) can auto trigger related sql transactions

Fetch Mode
- How to fetch related entities (right now or later?)
- OneToMany default: Lazy
- ManyToOne default: Eager (naturally)

N+1 select problem

logging.level.org.hibernate.type.descriptor.sql=trace
loggin.linin

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
