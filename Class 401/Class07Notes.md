# ***Interfaces***                                                                                                        

# Interfaces - Define Behavior for Multiple Types

**Article**
Date: 03/17/2023
Contributors: 4

An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement. Interfaces may define static methods that require implementation. Default implementations can be provided for interface members. However, interfaces cannot declare instance data such as fields, auto-implemented properties, or property-like events.

Using interfaces, you can incorporate behavior from multiple sources into a class. This is particularly important in C# due to the lack of support for multiple inheritance of classes. Interfaces are also necessary to simulate inheritance for structs, as they cannot directly inherit from another struct or class.

## Defining an Interface

An interface is defined using the `interface` keyword, as demonstrated in the following example:

```csharp
interface IEquatable<T>
{
    bool Equals(T obj);
}
```
Interface names should be valid C# identifiers and typically start with a capital "I".

Any class or struct implementing the IEquatable<T> interface must provide a definition for an Equals method matching the specified signature. This ensures that a class implementing the interface can determine whether it's equal to another instance of the same class.

Interface Implementation and Members
Interfaces can contain instance methods, properties, events, and indexers, as well as static constructors, fields, constants, or operators (starting from C# 11). Interface members are public by default, but you can specify other accessibility modifiers. Interface members must have a default implementation.

To implement an interface member, the corresponding member in the implementing class must be public, non-static, and have the same name and signature as the interface member.

When an interface declares static members, a type implementing the interface may also declare static members with the same signature. The static member in a type does not override the one declared in the interface.

## Implementing an Interface
A class or struct implementing an interface must provide implementations for all declared members without default implementations from the interface. If a base class implements an interface, any derived class inherits that implementation.

Here's an example implementation of the IEquatable<T> interface:

```csharp
Copy code
public class Car : IEquatable<Car>
{
    public string? Make { get; set; }
    public string? Model { get; set; }
    public string? Year { get; set; }

    // Implementation of IEquatable<T> interface
    public bool Equals(Car? car)
    {
        return (this.Make, this.Model, this.Year) == (car?.Make, car?.Model, car?.Year);
    }
}

```
## Additional Notes

Properties and indexers in a class can have extra accessors compared to those defined in an interface.
Interfaces can inherit from one or more interfaces, and a class implementing a derived interface must implement all members from base interfaces.
A base class can implement interface members using virtual members, which can be overridden by derived classes.

## Summary

An interface can define a group of related functionalities that classes or structs must implement.
Starting from C# 8.0, interfaces can provide default implementations for some or all of their members.
Interfaces cannot be directly instantiated; their members are implemented by classes or structs.
A class can implement multiple interfaces and inherit from a base class simultaneously.


# Back to Basics: Interfaces and Their Correct Usage

## Introduction

This article marks the beginning of the "Back to Basics" series, focusing on fundamental concepts that might require reevaluation. A core principle that demands our attention is the usage and understanding of interfaces. While widely employed in languages like C# and Java, interfaces might not always be utilized correctly. It's time to revisit their value and purpose.

## The Problem Interfaces Solve

Before diving into current interface usage, let's reexamine the fundamental problem interfaces intend to solve: **separating how something is used from how it's implemented**. This separation enables writing code that works with diverse implementations of certain responsibilities without handling each implementation explicitly.

To simplify, imagine a `Driver` class. Ideally, this class should be capable of a method like `Drive`, which can operate various types of vehicles like cars, boats, etc., by implementing the `IDriveable` interface. The `Driver` class shouldn't need separate methods like `DriveBoat`, `DriveCar`, etc., for each vehicle type.

## Interfaces Are Contracts

Interfaces serve as contracts that classes must adhere to. Implementing an interface guarantees that the class supports all methods defined in that interface. It's essential to differentiate between concrete inheritance and interface implementation. Concrete inheritance implies "Car is an Automobile," whereas an interface asserts "Car implements the Drivable interface." Classes can implement multiple interfaces, unlike concrete inheritance.

## Correct Use of Interfaces

**Interfaces Are Always Implemented by More Than One Class:** Correctly used interfaces are typically implemented by more than one class. When designing interfaces, it's crucial to focus on solving specific problems. Adding unnecessary interfaces to every class goes against the principle of "You Ain't Gonna Need It" (YAGNI). Only add interfaces when there's an actual need to solve a particular issue.

**Interfaces and Anticipation:** Anticipating future needs by adding interfaces prematurely can lead to overengineering. YAGNI suggests waiting until there's a genuine requirement before implementing an interface.

## Challenges with Testing and Dependency Injection

Though unit testing and dependency injection justify interface creation, their abuse can lead to incorrect usage.

**Abusing Interfaces for Testing:** While creating interfaces for mockability and testing might seem beneficial, it can overcomplicate the codebase. This approach creates an unnecessary level of indirection, making classes appear decoupled while they are not.

**Dependency Injection and Interface Abuse:** Dependency injection (DI) also faces the problem of interface abuse. Creating interfaces solely for injecting a single implementation can hinder performance and create unnecessary indirection.

## Overcoming Interface Abuse

The real challenge lies in unit testing and dependency injection practices that sometimes necessitate interface abuse. A solution involves genuinely splitting classes and reducing dependencies, rather than creating interfaces solely for the sake of DI. The ultimate goal is to replace implementations seamlessly during runtime, a feature not inherently supported by interfaces.

## Conclusion

Understanding interfaces' core purpose and using them judiciously is essential. Interfaces solve specific problems and should be employed only when necessary. Overusing interfaces for testing or DI can lead to unnecessary complexity and reduced interface potency. As developers, it's vital to ensure that interfaces remain a tool for solving problems and maintaining a balance between flexibility and simplicity.


# Understanding Interfaces in C#

An **interface** defines a contract that any class or struct implementing it must adhere to. Interfaces play a crucial role in creating a common framework for multiple classes or structs to provide specific behavior.

## Interface Basics

An interface may contain declarations for various members like methods, properties, indexers, events, and more. Classes and structs that implement an interface are required to provide implementations for all members declared in that interface.

Here's an example of a simple interface:

```csharp
interface ISampleInterface
{
    void SampleMethod();
}
```
In this example, any class or struct implementing ISampleInterface must provide an implementation for the SampleMethod method.

## Interface Implementation
When a class or struct implements an interface, it must provide concrete implementations for all the members declared in that interface. Here's an example:

```csharp
Copy code
class ImplementationClass : ISampleInterface
{
    public void SampleMethod()
    {
        // Method implementation.
    }
}
```
In this example, ImplementationClass implements the ISampleInterface and provides an implementation for the SampleMethod.

## Interface Usage
Interfaces allow you to define a common set of behaviors that classes or structs can adhere to. This facilitates writing flexible and modular code. For instance, you can create methods that accept interface instances and work with any class or struct that implements that interface.

```csharp
Copy code
static void UseSample(ISampleInterface instance)
{
    instance.SampleMethod();
}
```
Here, the UseSample method accepts any instance that adheres to the ISampleInterface, regardless of the actual class or struct type.

## Default Interface Members
Interfaces can also provide default implementations for some of their members. These default implementations are useful when multiple classes or structs implement the same behavior. Starting with C# 11, you can use static abstract or static virtual members to enforce specific implementations in implementing types.

## Interface Inheritance
Interfaces can inherit from other interfaces, allowing you to create a hierarchy of contracts. A class or struct implementing a derived interface must also implement all members of the base interfaces. When implementing an interface that inherits from another interface, use explicit interface implementation for overridden methods.

## Conclusion
Interfaces play a vital role in creating a contract-based structure in C#. They define a set of behaviors that implementing classes or structs must adhere to. This approach promotes flexibility and modularity in your codebase, allowing you to write more reusable and extensible software.