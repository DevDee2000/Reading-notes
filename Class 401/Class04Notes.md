# Reference Types in C#

- A type defined as a class is a reference type in C#.
- When you declare a variable of a reference type, it initially contains the value `null`.
- To create an instance of a class, use the `new` operator or assign an object of a compatible type.

## Declaring Classes

- Classes are declared using the `class` keyword followed by a unique identifier.
- An optional access modifier can precede the `class` keyword.
- Class members such as fields, properties, methods, and events are defined in the class body.

## Creating Objects

- A class and an object are different things.
- Objects can be created using the `new` keyword followed by the class name.
- An object is a concrete instance of a class.

## Constructors and Initialization

- Constructors are used to initialize objects when they are created.
- .NET types have default values, but you can provide initial values using field initializers or constructors.
- C# 12 introduced primary constructors as part of the class declaration.
- The `required` modifier on properties forces callers to set initial property values using object initializers.

## Class Inheritance

- C# supports class inheritance, allowing a class to inherit data and behavior from a base class.
- A base class is specified using a colon and the name of the base class after the derived class name.
- Classes can directly inherit from one base class and indirectly inherit from multiple base classes.
- Abstract classes define methods with a signature but no implementation and can't be instantiated.
- Sealed classes do not allow other classes to derive from them.

Note: Class definitions can be split between different source files using partial classes and methods.
