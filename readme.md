---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?
	member variables have values/objects unique to that instance of the class, as in if you create two objects the two will possibly have two different values and those will not interact. static class variables will instead be a single instance shared among all the instances of the class and the class itself. Any changes to one will change it for all.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
	It can make sense depending on whether you inform other developers to the public variable's existence or don't want them directly interacting with a variable made public for other reasons. It is necessary to make getters and setters for private variables though because unlike public they can only be accessed within the scope of that class.

3. What are some benefits of making member variables `private`?
	it prevents other other developers from 

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
	the super or parent class is class B, the sub class or child is class A

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
	it means that any variables or methods that the parent class has the sub class can use or 

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
	Concrete's require all classes to be implemented. Abstracts can have declared methods that will have to be implemented in any sub classes.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
	you can only declare methods in an interface, no implementations

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`	final means no subclassing so it would conflict with an abstract class which requires a concrete subclass. this is similar to the interaction between private and abstract for methods

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
	it means you have an exact copy of the method, same method signature and everything, and it is implemented in both (though I'm not sure if you can also override an abstract method. The "@Override" seems to be ok with using it above an implemented abstract method). If you call it on the child class it runs the child class's version.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
	List is an interface while LinkedList and ArrayList both implement that interface. you call it polymorphic because it can use any type of class that implements List and use it without casting by relying the definitions of methods within the interface. this is useful for not needing to know the exact type of class you are using at runtime but still get the desired functionality within whatever method you're using.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
