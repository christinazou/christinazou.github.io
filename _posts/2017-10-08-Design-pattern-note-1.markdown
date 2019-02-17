---
layout: post
title: Note - Design Pattern
date: 2017-10-08 12:30:10 -0700
description: a note for Design Pattern. I found several reading materials on the internet and a course on Coursera. Here is what I learned. # Add post description (optional)
tags: [Design Pattern]
---

**Design Pattern is actual solutions used in industrial software.** Over the years, developers have experimented with a variety of design solutions, and Desigh Pattern is a set of solutions that often create the best outcome. Each Design pattern has created for a particular purpose. The scope of application is as important as the solution itself.

**Design Pattern is more about concepts than coding templates.** It is a guideline to make the code more reusable and to prevent mistakes.
>Design patterns are defined by their purpose or intent, and not the exact code

**Design Pattern makes communication more effective and prevents misunderstanding.** Design Pattern give a name for each pattern, so developers do not have to repeat all the details in communication. 
>Prior knowledge of particular pattern not only give info about the solution, it also describes the original problem. Knowledge of design patterns leaves less room for misunderstanding. 

All the material I went through is written in Java, only because that I am more familiar with Java. Design Pattern applies to all object-oriented language. However, Design Pattern is essential to Java learning. Many Java frameworks are built upon Design Pattern. If you are going to read the document of Java framework like Spring, instead of starting right away, you might want to understand knowledge of Design Pattern first.

## Category of Design Pattern

>Creational Patterns tackle how you handle creating new objects.
>
>Structural patterns describe how objects are connected to each other. There are many different ways you can structure objects depending on the relationship you'd like between them. Not only do structural patterns describe how different objects have relationships, but also how subclasses and classes interact through inheritance.
>
>These patterns focus on how objects distribute work.They describe how each object does a single cohesive function. Behavioral patterns also focus on how independent objects work towards a common goal.

* Creational Design Patterns
	* [Singleton Pattern](#singleton-pattern)
	* [Factory Pattern](#factory-pattern)
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

## <a name="singleton-pattern">Singleton Pattern</a>

Singleton Pattern is to make sure there is only one instance in whole application, such as setting file. 

to enforce instantiation of only one object of a class
to provide global access to an object

Give the Singleton class a private constructor
Write a method that can create a new Singleton object or return the existing one.

key elements:
* A private constructor of Singleton class.
* A private class variable refering to the one instance of your Singleton class.
* A public method in the class that will create an instance of this class, but only if an instance does not exist already.

## <a name="factory-pattern">Factory Pattern</a>

Factory class creates objects like a real factory creates products. There are different categories and products can send to different stores.

key elements:
* A method in Factory class.
* In the method declares a product variable, which will refer to the knife object to be created.
* In the method the conditionals determine which subclass of product is actually instantiated.

the Factory method approach is described in the book of the gang of four.

## Facade Pattern

Facade Pattern provides a easy way for client code to interact with a complex system.

key elements:
* Design the interface.
* Implement the interface with one or more classes.
* Create the facade class and wrap the classes that implement the interface.
* A facade class can be used to wrap all the interfaces and classes for a subsystem.
* The intances, which of the classes that implement the interface, in facade class should be pravite.

## Adapter Pattern

>Generally the adapter pattern transforms one interface into another. The adapter pattern is usually used when you don't have control over the original class. 

One way to implement Adapter Pattern is to use wrapper classes that implement a unified interface to wrap the original classes.

key elements:
* Original class.
* Design the interface.
* Implement wrapper class using the interface
* In wrapper class, a class variable refering to a instance of the original class
* In wrapper class, the implementation of methods delegate to methods of the original class

## Composite Pattern

Composite Pattern helps create a structure, which consists of instances of composite classes. we could imagine it as a big triangle consist by smaller triangles, and these triangles are consist of even more smaller triangles.

key elements:
* Design the interface.
* Define subclasses implement interface.
* The sublclass could include instances of class that implement the same interface. if so, the subclass need to provide iterate add delete function of these instance.

## Proxy Pattern 

The proxy design pattern allows a proxy class to act as a placeholder to represent a real subject class.

key elements:
* Both the proxy class and the real subject class implement a common subject interface.
* The proxy class and the real subject class will implement the interface differently.

## Decorator Pattern

Decorator Pattern allows object to dynamically add behaviors to others.

key elements:
* Design the interface.
* Create concrete classes implementing the  interface.
* Create abstract decorator class implementing the same interface.
* The abstract decorator class will concrete the class implementing the interface.
* Create concrete decorator class extending the abstract decorator class.

## Template Method Pattern

>The template method pattern is a practical application of generalization and inheritance. 

key elements:
* A public template method and abstract methods in the superclass.
* The template methode will use a general set of steps.
* The common method of subclasses will be implemented in superclass.
* These methods are special to each subclass will be implemented in the subclass.

## Chain of Responsibility Pattern

key elements:
* A public template method and abstract methods in the superclass.
* The template methode will use a general set of steps.
* The common method of subclasses will be implemented in superclass.
* These methods are special to each subclass will be implemented in the subclass.

## command pattern

>One purpose of using the command pattern is to store and schedule different requests. you can not store or manage methode call, but turning these request into command objects can allow you to treat them as the way you would treat other objects. 
>
>Another main benefit of the command pattern is that it decouples the objects of your software program. When you have a class that wants to make a request, that class doesn't need to know about the other objects in the software system.
>
>The command pattern also allows you to pull out logic from your user interfaces. Usually, code-to-handle requests is put into the event handlers of user interfaces. However, it doesn't really make sense to have a lot of application logic sitting in your user interface classes. The user interface classes should only be dealing with user interface issues like getting information to and from the user. Instead, the command pattern creates a new layer which is where these command objects will go. 

key elements:
* There need be a invoker to invoke these command, and a command manager to manege the command
* You have a command super-class and all commands will be instances of sub-classes of this command super-class. 
* Super-class defines the common behaviors of your commands. 
* Each command will have the methods execute, unexecute and isReversible. 
* The execute method will actually do the work that the command is supposed to do, 
* unexecute will do the work of undoing the command, and 
* isReversible determines if the command is reversible, returning true if the command can be undone. There could be some commands that can't be undone. 

## Observer Pattern

key elements:
* First, we'll have a Subject superclass that defines three methods, allow a new observer to subscribe, allow a current observer to unsubscribe, and notify all observers about a new blog post.This superclass would also have an attribute to keep track of all the observers,
* The blog Class will be a subclass of the Subject superclass.
* The observer interface will have a update method.
* the Subscriber Class will implement the observer interface. 

## Qustions

the Brige Pattern sound similar to Adapter Pattern and Facade Pattern. what the difference between them? why Brige Pattern is nessesery? 

What's the differ between Facade Pattern and Proxy Pattern?

What's the differ between Decorator Pattern and Template Method Pattern?

## References

Since the famous book "Design Pattern" written by the gang of four uses c++ as implementing language, I choose other material to look at instead. I read the tutorials form [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/) and [journaldev.com](https://www.journaldev.com/1827/java-design-patterns-example-tutorial), then I watched the vedios from [Design Patterns by University of Alberta](https://www.coursera.org/learn/design-patterns/home/welcome). 

This is a very clean explaination of [Adapter Pattern](https://stackoverflow.com/questions/1299167/understanding-adapter-pattern). 

When I was looking for more on the internet I found this web site [sourcemaking.com](https://sourcemaking.com/design_patterns). The defination of each Design Pattern is a little bit different from others. It's nice to have more perspective.

