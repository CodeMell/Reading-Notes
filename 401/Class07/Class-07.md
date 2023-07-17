# Interfaces

[Interfaces](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/interfaces)

- Interfaces can include static methods with implementations and can provide default implementations for members.

- C# does not support multiple inheritance of classes, so interfaces allow for incorporating behavior from multiple sources.

- Interfaces are also used to simulate inheritance for structs, which cannot directly inherit from another struct or class.

- Interfaces can contain instance methods, properties, events, indexers, and other member types, but they cannot include instance fields, constructors, or finalizers.

- Implementing classes or structs must provide implementations for all declared members of an interface.

- Properties and indexers of a class can have additional accessors compared to those defined in an interface.

- Interfaces can inherit from one or more interfaces, and a class implementing a derived interface must implement all members from the derived and base interfaces.

- An interface cannot be instantiated directly, but its members are implemented by classes or structs that implement the interface.

- A class or struct can implement multiple interfaces while also inheriting from a base class.

interfaces provide a way to define a common set of behaviors that different classes or structs can implement, enabling code reusability and flexibility in C# programming.

[Back to Basics](https://simpleprogrammer.com/back-to-basics-what-is-an-interface/)

- The purpose of an interface is to separate how something is used from how it is implemented. It allows code to work with different implementations of a set of responsibilities without specifically handling each implementation.

- Interfaces serve as contracts, specifying that a class meets certain expectations and supports all the methods defined in the interface.

- Unlike concrete inheritance, where a class is considered to be a specific type, implementing an interface means that the class fulfills the contract defined by the interface.

- Interfaces are designed to solve specific problems and should only be implemented by more than one class when there is a genuine need. Creating interfaces for every class, regardless of necessity, is not recommended.

- The ratio of interfaces to implementing classes should ideally be close to 1 to 1. Creating interfaces in anticipation of future needs violates the YAGNI (You Ain't Gonna Need It) principle.

- The misuse of interfaces often occurs when trying to facilitate unit testing or dependency injection. While these are valid use cases, creating interfaces solely for the purpose of mocking or injecting dependencies can lead to unnecessary indirection and coupling.

- The author suggests focusing on reducing dependencies and splitting classes apart instead of relying on interfaces as a workaround for testing or dependency injection challenges.

- The article concludes by stating that a language-supported mechanism is needed to easily replace implementations of concrete classes at runtime, rather than relying on interfaces as a trick to achieve this.

emphasizes using interfaces purposefully, avoiding excessive and unnecessary interface usage, and considering alternative approaches to address testing and dependency injection challenges.

[Interfaces #2](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/interface)

- An interface defines a contract that any class or struct implementing it must adhere to.

- Interfaces can include methods, properties, indexers, events, and more. They can also have default implementations for some or all of their members.

- Beginning with C# 11, interfaces can declare static abstract and static virtual members, allowing them to define common functionality for implementing types.

- Interfaces can inherit from other interfaces, but they cannot contain instance state or instance auto-properties.

- Classes implementing an interface must provide an implementation for all the members defined in the interface.

- Explicit interface implementation is possible, where members of an interface are implemented explicitly and can only be accessed through an instance of the interface.

- Interfaces are used to achieve abstraction and decoupling in code, allowing for flexibility and code reuse.

interfaces in C# provide a way to define contracts and ensure consistent behavior among different classes or structs, promoting modularity and flexibility in code design.