# Inheritance - Derive Types to Create More Specialized Behavior

## Abstract and Virtual Methods

- Abstract methods must be overridden in non-abstract derived classes.
- Virtual methods can be overridden in derived classes with their own implementation.
- Abstract and virtual methods are the basis for polymorphism.

## Abstract Base Classes

- Abstract classes prevent direct instantiation and must be derived from.
- Abstract classes can contain abstract methods with no implementation.
- Derived classes that aren't abstract must implement all abstract methods.

## Interfaces

- Interfaces define a set of members that implementing classes and structs must implement.
- A class can implement multiple interfaces but can only have one direct base class.
- Interfaces are used to define specific capabilities, not necessarily "is a" relationships.

## Preventing Further Derivation

- A class can prevent other classes from inheriting from it or its members by using the `sealed` keyword.

## Derived Class Hiding of Base Class Members

- A derived class can hide base class members by declaring members with the same name and signature.
- The `new` modifier can be used to explicitly indicate that the member is not an override of the base member.
- Using `new` isn't required but will generate a compiler warning if not used.


# Abstract and Sealed Classes and Class Members (C# Programming Guide)

## Abstract Classes and Class Members

- The `abstract` keyword enables the creation of incomplete classes and class members that must be implemented in a derived class.
- An abstract class cannot be instantiated and is designed to provide a common definition of a base class that multiple derived classes can share.
- Abstract classes may define abstract methods using the `abstract` keyword, which have no implementation and must be implemented by derived classes.
- Derived classes of an abstract class must provide implementations for all abstract methods.
- An abstract class can override a virtual method from a base class with an abstract method.

Example:
```csharp
public abstract class A
{
    // Class members here.
}

public abstract class B
{
    public abstract void DoWork(int i);
}

public class C : B
{
    public override void DoWork(int i)
    {
        // Implementation in derived class.
    }
}
```
## Sealed Classes and Class Members
- The sealed keyword prevents a class from being used as a base class, disallowing further derivation from it.
- Sealed classes cannot be abstract, and they cannot be used as base classes.
- Sealed classes prevent inheritance and can make calling sealed class members slightly faster.
- A method, indexer, property, or event, on a derived class that is overriding a virtual member of the base class can be declared as sealed,preventing any further overriding.

Example: 

```csharp
public sealed class D
{
    // Class members here.
}

public class E
{
    public virtual void DoWork()
    {
        // Original implementation.
    }
}

public class F : E
{
    public sealed override void DoWork()
    {
        // New implementation, sealed to prevent further overriding.
    }
}
```

# Polymorphism

Polymorphism is a fundamental concept in object-oriented programming and is considered the third pillar, alongside encapsulation and inheritance.

## Aspect 1: Object Casting

- At runtime, objects of a derived class can be treated as objects of a base class in method parameters, collections, or arrays.
- The object's declared type may differ from its runtime type due to this polymorphic behavior.

## Aspect 2: Virtual Methods

- Base classes can define and implement virtual methods, which derived classes can override with their own implementations.
- When client code calls a virtual method, the CLR looks up the runtime type of the object and invokes the appropriate override of the virtual method.

## Application of Polymorphism

To work with groups of related objects in a uniform way, you can use polymorphism to:

1. Create a class hierarchy with a common base class and derived classes representing specific shapes.
2. Implement a virtual method, such as `Draw()`, in the base class and override it in each derived class to draw the specific shape.
3. Store instances of derived classes in a collection of the base class type (`List<Shape>` in this example) and call the `Draw()` method on each object in the collection.

Example Code:
```csharp
public class Shape
{
    // ... members ...

    public virtual void Draw()
    {
        Console.WriteLine("Performing base class drawing tasks");
    }
}

public class Circle : Shape
{
    public override void Draw()
    {
        // ... draw circle ...
        Console.WriteLine("Drawing a circle");
        base.Draw();
    }
}

public class Rectangle : Shape
{
    public override void Draw()
    {
        // ... draw rectangle ...
        Console.WriteLine("Drawing a rectangle");
        base.Draw();
    }
}

public class Triangle : Shape
{
    public override void Draw()
    {
        // ... draw triangle ...
        Console.WriteLine("Drawing a triangle");
        base.Draw();
    }
}

// Usage:
var shapes = new List<Shape>
{
    new Rectangle(),
    new Triangle(),
    new Circle()
};

foreach (var shape in shapes)
{
    shape.Draw();
}
```

### Virtual Members

- Derived classes can override virtual members to define new behavior or preserve the existing behavior for further overrides.
- Fields cannot be virtual; only methods, properties, events, and indexers can be virtual.
### Hiding Base Class Members

- Use the new keyword to hide base class members with members of the same name in the derived class.
- Hidden base class members can still be accessed by casting the derived class instance to the base class type.
### Preventing Virtual Method Inheritance

- A derived class can stop virtual inheritance by declaring an override as sealed.
- Sealed methods can be replaced by derived classes using the new keyword.
### Accessing Base Class Virtual Members

- A derived class that has overridden a method or property can still access the base class's implementation using the base keyword.
- It is recommended to use base to call the base class implementation in derived class overrides, enabling the derived class to focus on specific behavior while ensuring compatibility with the base class behavior.


# Object-Oriented Programming (C#)

C# is an object-oriented programming language, and it follows four basic principles of object-oriented programming:

## 1. Abstraction

- Abstraction involves modeling relevant attributes and interactions of entities as classes to create an abstract representation of a system.
- It helps in hiding unnecessary details and focuses on the essential characteristics of an object.
- The BankAccount class provided an example of abstraction, representing the concept of a bank account.

## 2. Encapsulation

- Encapsulation involves hiding the internal state and functionality of an object and only allowing access through a public set of functions.
- It helps in protecting the integrity of the object and allows for better code maintenance.
- The BankAccount and Transaction classes demonstrated encapsulation by providing controlled access to the internal data and methods.

## 3. Inheritance

- Inheritance allows creating new abstractions based on existing abstractions.
- It enables a class to acquire properties and methods from another class, known as the base class.
- The new bank account types (InterestEarningAccount, LineOfCreditAccount, and GiftCardAccount) inherited from the BankAccount class, reusing its behavior while adding new functionality.

## 4. Polymorphism

- Polymorphism enables implementing inherited properties or methods in different ways across multiple abstractions.
- It allows treating objects of different derived classes as objects of their common base class, providing flexibility and reusability.
- The article showcased polymorphism in the PerformMonthEndTransactions method, which was overridden in derived classes to perform specific actions based on the account type.

### Creating Different Types of Accounts

- The article explained how to create different types of accounts (InterestEarningAccount, LineOfCreditAccount, and GiftCardAccount) using inheritance.
- Derived classes were defined with new functionality, extending the base BankAccount class.

### Constructor Chaining

- Constructor chaining was utilized to provide multiple constructors for initializing objects with different parameters efficiently.

### Virtual Methods and Overriding

- Virtual methods were used in the BankAccount class, allowing derived classes to override their behavior using the `virtual` and `override` keywords, respectively.

### Protected Access Modifier

- The `protected` access modifier was used to limit access to certain methods, enabling only derived classes to call them.

### Polymorphic Behavior

- Polymorphism was demonstrated in the LineOfCreditAccount class, where the `CheckWithdrawalLimit` method was overridden to charge a fee for overdrafts.

### Summary

- The tutorial provided a comprehensive overview of object-oriented programming principles in C#, showcasing abstraction, encapsulation, inheritance, and polymorphism.
- By applying these principles, the article illustrated how to create a hierarchy of classes to manage different types of bank accounts with shared and specific behavior.
