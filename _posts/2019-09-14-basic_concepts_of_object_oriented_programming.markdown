---
layout: post
title:      "Basic Concepts of Object Oriented Programming"
date:       2019-09-14 14:42:14 +0000
permalink:  basic_concepts_of_object_oriented_programming
---



The main principles of OOP are:
* abstraction
* encapsulation
* inheritance
* polymorphism

Abstraction is a mechanism in which you show only “relevant” data and “hide” the details of an object from the user. For example, when you  transfer money from your online bank to another account, you enter the amount and the destination. What happens after you press the confirm button and how the money is transferred is abstracted away for you.

Encapsulation keeps classes separated which is essential in dividing responsibilities in programming. This comes especially useful in large applications. It hides the details of how the class is implemented from other objects.
You encapsulate by making your class attributes inaccessible from the outside and by providing getter and/or setter methods for attributes that are accessible by other classes.

Inheritance is the principle by which an object inherits some or all properties of another object. For example, a Car class can have sublcasses of Sedan, and Coupe. Sedan and Coupe acquire the properties of Car. Sedan also has some properties such as four-doors which would be differ from the Coupe which has two doors. These specific properties are not inherited from the Car class.

Polymorphism means "many forms". It describes a pattern in OOP in which classes have different functionality while sharing a common interface. For example, we have a class called Animal and subclasses Duck, Dog, and Cat inherit from Animal and all have a makeNoise method. If we create animal=Duck.new(), the result of animal.makeNoise will be different if we declared animal =Dog.new(). 

 
