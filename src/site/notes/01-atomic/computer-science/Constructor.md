---
{"dg-publish":true,"permalink":"/01-atomic/computer-science/constructor/","tags":["cs/oop","university/INF201"],"dg-note-properties":{"tags":["cs/oop","university/INF201"],"aliases":["ctor"],"source":["https://en.wikipedia.org/wiki/Constructor_(object-oriented_programming)"]}}
---

# Constructor
In [[01-atomic/computer-science/Object-Oriented Programming\|Object-Oriented Programming]], a constructor is a special type of [[01-atomic/computer-science/Method\|Method]] for a [[01-atomic/computer-science/Class\|Class]] called to create an [[01-atomic/computer-science/Object\|Object]] from the class it's created.

It differs from a common method, but differs in:
- Doesn't have an explicit return type
- It's not implicitly [[Inheritance\|Inherited]]
- Has different rules for [[Access Identifiers\|Access Identifiers]].

It's common to have [[01-atomic/computer-science/Function Overloading\|Overloading]] the constructor with different [[Parameter\|Parameters]]
## Types of Constructors
- [[Factory Constructor\|Factory Constructor]]
- [[01-atomic/computer-science/Copy Constructor\|Copy Constructor]]: When there's dynamic memory, it's common to implement a constructor to copy the data if the object is copied (see [[Rule Of Three\|Rule Of Three]])
