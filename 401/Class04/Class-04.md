# Classes & Memory Management
[Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)

[Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)

[Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)

What’s the difference between a static and an instance constructor?
The main difference between a static constructor and an instance constructor in C# is their purpose and behavior:

Purpose:
- Instance Constructor: An instance constructor is used to initialize the instance (object) of a class. It is called when an object is created using the new keyword.
- Static Constructor: A static constructor is used to initialize the static members of a class. It is called only once, before any instance of the class is created or any static member is accessed.

Invocation:
- Instance Constructor: An instance constructor is invoked explicitly by using the new keyword to create an object of the class. Each object has its own instance constructor that is called independently for each object.
- Static Constructor: A static constructor is invoked automatically by the runtime before any static member is accessed or any instance of the class is created. It is called only once for the entire lifetime of the application domain.

Signature and Access Modifier:
- Instance Constructor: An instance constructor has the same name as the class and can have parameters. It doesn't have a return type. The access modifier can be specified (e.g., public, private, protected, internal, etc.).
- Static Constructor: A static constructor has the same name as the class and doesn't take any parameters. It doesn't have a return type. The access modifier is always private, and it cannot be explicitly specified.

Usage:
- Instance Constructor: An instance constructor is used to initialize the instance fields and properties of a class. It can contain custom initialization logic specific to each object.
- Static Constructor: A static constructor is used to initialize the static fields and perform one-time initialization tasks for the class. It is often used to initialize static resources, set default values, or perform other initialization that needs to be done only once.

How does the use of a static constructor differ from setting properties/values?



[Stack and Heap](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)

Knowing what you now know about the stack and the heap, how might you rethink the way you did projects in previous courses, to make more effecient use of memory?

[Garbage Collection Fundamentals](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)

Compare “Garbage Collection” in C# with the lifecycle of normal household items.