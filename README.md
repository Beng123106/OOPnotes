#Basics
A class is an abstract description of something that could exist with certain attributes/methods (eg. a dog class may have age/gender/breed)
An object is sort of like something that contains data and code that exists under a class
Classes can have unique methods, you declare them like you would a new function 
__init__ initializes the objects attributes (makes it so you can actually work with the attributes)
self paramater allows you to refer to the object

##Useful terminology/things you can do
Encapsulation restricts access to certain attributes and methods (__ as as prefix)
Overloading is when there is two methods that belong to the same class, but have different parameters
Overriding is when two methods have the same name but perform different tasks
Polymorphism is when a method exists across different classes and objects 

__repr__ presents a printable version of our object
__str__ converts the object to a string
What is the difference? I honestly do not know. I guess if you want to use your object as a string then do __str__, otherwise if you just want to print it out use __repr__?

###Inheritance
When an object or class is based on another object/class
Single inheritance: a subclass inheriting from a single superclass/parent class
Multiple inheritances: subclass that has multiple parent classes
Multilevel inheritance: a subclass that is inheriting from another subclass that is inheriting from a....
Subclass does not need __init__ unless it needs new attributes
the super() method refers to the parent class

Whats the point of inheritance?
subclass will recieve all attributes and methods
the subclass can build on and enhance itself with more attributes and methods
a subclass can override methods/attributes they inherit

####Iterable objects
raise is a keyword to raise an exception (raise StopIteration)
__iter__ allows the object to be iterable
__next__ allows you to get to the next value 

Deck of cards example that demonstrates this:
```python
class Deck:
	… Code …
	def __iter__(self):
		return self

	def __next__(self):
		self.__index += 1
		if self.__index == len(self.__cards):
			self.__index = -1 # index reset
			raise StopIteration
		else:	
			return self.__cards[self.__index]

```
