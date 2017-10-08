---
layout: post
title: Design Pattern note 1
date: 2017-10-08 00:00:00 +0300
description: a note for Design Pattern. I found several reading materials on the internet and a course on Coursera. Here is what I learned. # Add post description (optional)
tags: [Design Pattern]
---

**Design Pattern is actual solutions used in industrial software.** Over the years, developers have experimented with a variety of design solutions, and Desigh Pattern is a set of solutions that often create the best outcome. Each Design pattern has created for a particular purpose. The scope of application is as important as the solution itself.

**Design Pattern is more about concepts than coding templates.** It is a guideline to make the code more reusable and to prevent mistakes.

**Design Pattern Design Pattern makes communication more effective and prevents misunderstanding.** Design Pattern give a name for each pattern, so developers do not have to repeat all the details in communication. Prior knowledge of particular pattern not only give info about the solution, it also describes the original problem. Knowledge of design patterns leaves less room for misunderstanding. 

All the material I went through is written in Java, only because that I am more familiar with Java. Design Pattern applies to all object-oriented language. However, Design Pattern is essential to Java learning. Many Java frameworks are built upon Design Pattern. If you are going to read the document of Java framework like Spring, instead of starting right away, you might want to understand knowledge of Design Pattern first.

### Category of Design Pattern

>Creational Patterns tackle how you handle creating new objects.
>
>Structural patterns describe how objects are connected to each other. There are many different ways you can structure objects depending on the relationship you'd like between them. Not only do structural patterns describe how different objects have relationships, but also how subclasses and classes interact through inheritance.
>
>These patterns focus on how objects distribute work.They describe how each object does a single cohesive function. Behavioral patterns also focus on how independent objects work towards a common goal.

* Creational Design Patterns
	* Singleton Pattern
	* Factory Pattern
	* Abstract Factory Pattern
	* Builder Pattern
	* Prototype Pattern
* Structural Design Patterns
	* Adapter Pattern
	* Composite Pattern
	* Proxy Pattern
	* Flyweight Pattern
	* Facade Pattern
	* Bridge Pattern
	* Decorator Pattern
* Behavioral Design Patterns
	* Template Method Pattern
	* Mediator Pattern
	* Chain of Responsibility Pattern
	* Observer Pattern
	* Strategy Pattern
	* Command Pattern
	* State Pattern
	* Visitor Pattern
	* Interpreter Pattern
	* Iterator Pattern
	* Memento Pattern

### Singleton Pattern

Singleton Pattern is to make sure there is only one instance in whole application, such as setting file. 

element:
private constructor of Singleton class.
private class variable refering to the one instance of your Singleton class.
public method in the class that will create an instance of this class, but only if an instance does not exist already.

### Factory Pattern

Factory class create objects like real factory create products, there are different categories and products can send to different stores.

must have element:

### Composite Pattern

Composite Pattern helps create a tree-sharp structure, which consists of instances of composite class, each works as a tree node.

must have element: 

Since the famous book "Design Pattern" written by the gang of four uses c++ as implementing language, I choose other material to look at instead. I read the tutorials form [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/) and [journaldev.com](https://www.journaldev.com/1827/java-design-patterns-example-tutorial), then I watched the vedios from [Design Patterns
by University of Alberta](https://www.coursera.org/learn/design-patterns/home/welcome). 


