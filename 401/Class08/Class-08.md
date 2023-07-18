# Collections & Enums

## [Collections](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/collections)

- There are two ways to group objects: using arrays and using collections.

- Arrays are useful for working with a fixed number of strongly typed objects, while collections provide more flexibility as they can dynamically grow and shrink.

- Collections allow you to assign keys to objects for quick retrieval.

- Collections are classes, so you need to declare an instance of the class before adding elements to the collection.

- The `System.Collections.Generic` namespace provides generic collection classes that enforce type safety and are recommended for collections with a single data type.

- Common generic collection classes include `List<T>`, `Dictionary<TKey, TValue>`, `Queue<T>`, `Stack<T>`, and `SortedList<TKey, TValue>`.

- The `System.Collections.Concurrent` namespace provides thread-safe collection classes for concurrent access from multiple threads.

- The `System.Collections` namespace provides legacy collection classes that store objects as `Object` types, but it's recommended to use generic collections instead.

- Custom collections can be implemented by implementing the `IEnumerable<T>` or `IEnumerable` interface.

- LINQ (Language-Integrated Query) can be used to query and manipulate collections.

- Collections can be sorted by implementing the `IComparable<T>` interface and using the `Sort` method or by using LINQ.

- Custom collections can be defined by implementing the `IEnumerable` interface and using iterators, which allow custom iteration over the collection.

- Iterators are methods or get accessors that use the `yield return` statement to return elements one at a time.

- Iterators are called using a `foreach` statement, and execution is resumed from the last `yield return` statement each time the iterator is called.

## [Enums](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/enum)

- An enumeration type, or enum type, is a value type in C# defined by a set of named constants of an underlying integral numeric type.

- To define an enum type, you use the `enum` keyword followed by the names of the enum members.

- By default, the associated constant values of enum members are of type `int` and start with zero, increasing by one in the order of definition.

- You can explicitly specify any other integral numeric type as the underlying type of an enum.

- You can also explicitly specify the associated constant values for enum members.

- Methods cannot be defined inside the definition of an enum type; instead, you can add functionality to an enum type by creating an extension method.

- The default value of an enum type is the value produced by `(E)0`, even if zero doesn't correspond to an enum member.

- Enum types are used to represent a choice from a set of mutually exclusive values or a combination of choices.

- To represent a combination of choices, you can define enum members as bit fields, where the associated values are powers of two.

- Bitwise logical operators (`|` and `&`) can be used to combine or intersect enum choices respectively.

- The `Flags` attribute can be applied to an enum type to indicate that it declares bit fields.

- The `System.Enum` type is the abstract base class of all enumeration types and provides methods to get information about enum types and their values.

- The `enum` constraint can be used to specify that a type parameter is an enumeration type.

- Conversions exist between an enum type and its underlying integral type, allowing casting between enum values and their associated integral values.

- The `Enum.IsDefined` method can be used to check if an enum type contains an enum member with a specific associated value.

- Boxing and unboxing conversions can be performed between an enum type and the `System.Enum` type.