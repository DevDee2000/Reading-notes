# ***Interfaces***                                                                                                        

- An interface in C# contains definitions for a group of related functionalities that a non-abstract class or struct must implement.
- Interfaces may define static methods, which require an implementation.
- Interfaces can provide a default implementation for members.
- Interfaces cannot declare instance data such as fields, auto-implemented properties, or property-like events.
- Interfaces are used to include behavior from multiple sources in a class, as C# does not support multiple inheritance of classes.
- An interface is defined using the `interface` keyword.
- Any class or struct implementing an interface must provide definitions for the members specified by the interface.
- Interfaces can contain instance methods, properties, events, indexers, static constructors, fields, constants, or operators.
- Interface members are public by default but can have explicit accessibility modifiers.
- To implement an interface member, the implementing class must have a corresponding member with the same name and signature.
- A class can implement multiple interfaces but can inherit from only one class.
- If a base class implements an interface, any derived class also inherits the implementation.
- Properties and indexers of a class can have extra accessors beyond what is defined in the interface.
- Interfaces can inherit from one or more interfaces, and a class implementing a derived interface must implement all members from the derived and base interfaces.
- An interface cannot be instantiated directly; its members are implemented by classes or structs that implement the interface.
- A class or struct can implement multiple interfaces and can also inherit from a base class.
- Beginning with C# 8.0, interfaces can define default implementations for some or all of their members.
