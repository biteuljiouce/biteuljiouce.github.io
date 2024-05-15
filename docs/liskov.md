Why Square Shouldn't Inherit from Rectangle
----

Liskov's Substitution Principle states that objects of a derived class should be usable interchangeably with objects of the base class without altering the program's behavior. However, when considering the relationship between the Rectangle and Square classes, we find an example where this rule is violated.

The fundamental issue lies in the invariants that define the Rectangle class compared to Square. A rectangle is defined by two dimensions, its length and width, which can be independently modified. In contrast, a square's sides are intrinsically linked; modifying the length must also modify the width to preserve the square's property.

To resolve this design problem, it's better to separate the concepts of Rectangle and Square into two distinct classes, each with its own invariants and specific methods. One approach is to use a common base class, such as Shape, to encapsulate properties and behaviors common to all geometric shapes while allowing each specific shape (Rectangle, Square, etc.) to implement its own functionality appropriately.

In conclusion, while the relationship between Rectangle and Square may seem intuitive at first glance, it actually violates Liskov's Substitution Principle. By restructuring the class hierarchy to adhere to this principle, we can create a more robust and flexible model for representing geometric shapes in our programs.