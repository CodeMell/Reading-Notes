# Object Oriented Principles

[Inheritance](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/inheritance)

- Inheritance, along with encapsulation and polymorphism, is one of the primary characteristics of object-oriented programming.

- Inheritance allows you to create new classes that reuse, extend, and modify the behavior defined in other classes.

- The class whose members are inherited is called the base class, and the class that inherits those members is called the derived class.

- A derived class can have only one direct base class, but inheritance is transitive, so a derived class inherits the members from its base class and all its base classes.

- Interface declarations may provide default implementations for their members, which are inherited by derived interfaces and classes implementing those interfaces.

- When a class derives from another class, it implicitly gains all the members of the base class except for constructors and finalizers.

- Derived classes can add their own members and extend the functionality of the base class.

- Abstract methods and virtual methods allow for method overriding in derived classes. Abstract methods must be implemented in non-abstract derived classes.

- Abstract base classes can prevent direct instantiation and can contain abstract members that must be implemented by derived classes.

- Interfaces define a set of members that implementing classes must implement. A class can implement multiple interfaces but can only directly inherit from one class.

- Sealed classes and members prevent further derivation or overriding by other classes.

- Derived classes can hide base class members by declaring members with the same name and signature, using the new modifier to indicate that it's not intended as an override.

 - Inheritance allows for code reuse, extensibility, and specialization in object-oriented programming, providing a powerful mechanism for structuring and organizing classes.

[Abstract](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members)

Abstract Classes and Class Members:

- Abstract classes are declared using the abstract keyword before the class definition.

- An abstract class cannot be instantiated and serves as a common base class for multiple derived classes.

- Abstract classes can contain abstract methods, which are declared using the abstract keyword before the return type.

- Abstract methods have no implementation and must be implemented in derived classes.

- Derived classes can override virtual methods from a base class with abstract methods.

- Abstract classes can force derived classes to provide new method implementations for virtual methods.

Sealed Classes and Class Members:

- Sealed classes are declared using the sealed keyword before the class definition.

- A sealed class cannot be used as a base class and cannot be an abstract class.

- Sealed classes prevent further derivation and can provide performance optimizations.

- Derived classes can mark a method, indexer, property, or event as sealed to prevent further overriding in subsequent derived classes.

abstract classes and sealed classes are useful features in C# that allow for the creation of class hierarchies and control over inheritance and method overriding.

[Polymorphism](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/polymorphism)

Polymorphism is a fundamental concept in object-oriented programming and is considered the third pillar along with encapsulation and inheritance. It has two aspects:

Polymorphic Behavior at Run-Time:

- Objects of a derived class can be treated as objects of the base class. This allows flexibility in method parameters, collections, and arrays.

- The declared type of an object may differ from its actual run-time type.

Virtual Methods and Method Overriding:

- Base classes can define virtual methods that can be overridden by derived classes. This allows derived classes to provide their own implementation of the method.
- At run-time, when a virtual method is called, the actual implementation invoked is determined by the run-time type of the object.
- Virtual methods enable working with groups of related objects in a uniform way.

polymorphism is a powerful concept that enables flexibility, extensibility, and uniformity in object-oriented programming by allowing objects to be treated in a generalized manner and providing the ability to override and customize behavior in derived classes.

[OOP Principles](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/object-oriented-programming)

four basic principles of OOP: abstraction, encapsulation, inheritance, and polymorphism:

- Abstraction: It involves modeling relevant attributes and interactions of entities as classes to define an abstract representation of a system. The BankAccount class mentioned in the article serves as an example of abstraction.

- Encapsulation: It involves hiding the internal state and functionality of an object and only allowing access through a public set of functions. The BankAccount and Transaction classes demonstrate encapsulation by encapsulating the components needed to describe the concepts in code.

- Inheritance: It allows creating new abstractions based on existing abstractions. Inheritance enables derived classes to inherit methods and data from a base class. The article introduces different types of bank accounts (e.g., InterestEarningAccount, LineOfCreditAccount, GiftCardAccount) that inherit from the BankAccount class to extend its functionality and behavior.

- Polymorphism: It allows implementing inherited properties or methods in different ways across multiple abstractions. Polymorphism enables objects of different derived classes to be treated as objects of their base class, allowing flexibility and customization. The article demonstrates polymorphism by creating a virtual method, PerformMonthEndTransactions(), in the BankAccount class and providing different implementations for it in derived classes.