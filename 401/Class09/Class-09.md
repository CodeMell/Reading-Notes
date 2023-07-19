# LINQ & Delegates

## [LINQ](https://learn.microsoft.com/en-us/dotnet/csharp/linq/)

- Language-Integrated Query (LINQ) is a set of technologies integrated into the C# language that allows developers to perform queries against various data sources using a common, declarative syntax. Traditionally, developers had to use different query languages for different data sources like SQL databases, XML documents, and web services, leading to a lack of type checking at compile time and making it challenging to switch between data sources.

- With LINQ, queries become a first-class language construct in C#, similar to classes and methods, making them type-safe and supporting IntelliSense. The most visible part of LINQ for developers is the query expression, which allows them to filter, order, and group data with minimal code. This query expression syntax can be used to query and transform data from LINQ-enabled sources like SQL databases, ADO.NET Datasets, XML documents, and .NET collections.



- Query Expression Overview: LINQ provides a declarative query syntax that is easy to understand and uses familiar C# language constructs. Variables in query expressions are strongly typed, and the compiler can often infer the type without explicit specification. Queries are executed only when iterated over, typically in a foreach statement.

- Query Syntax vs. Method Syntax: Query expressions are converted to Standard Query Operator method calls at compile time, but query syntax is usually more readable and concise. Developers are encouraged to use query syntax whenever possible and switch to method syntax when necessary, as there is no semantic or performance difference between the two forms.

- IQueryable LINQ Providers: LINQ supports querying both in-memory data and remote data sources. For in-memory data, developers can use LINQ to Objects by implementing IEnumerable<T> or extending the type with standard query operator methods. For remote data, the recommended approach is to implement the IQueryable<T> interface, although it requires more complexity than LINQ to Objects.

- Complexity of IQueryable Providers: IQueryable providers can vary in complexity. Simple providers may interact with a single method of a web service and have a closed type system. Medium complexity providers may target data sources with partially expressive query languages and have a richer type system. Complex providers, like LINQ to SQL, can translate complete LINQ queries to an expressive query language like SQL and have an open type system with extensive user-defined type mapping.

- LINQ simplifies data querying by integrating query capabilities directly into C# and providing a unified, expressive syntax for various data sources. Developers can use query expressions to filter and manipulate data with type safety, making code more readable and maintainable. LINQ also allows for querying both in-memory and remote data sources, making it a powerful tool for data manipulation and retrieval in C# applications.

## [Introduction To LINQ Queries](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)

LINQ (Language Integrated Query) is a feature in C# that provides a consistent way to query and manipulate data from various data sources, such as databases, XML documents, collections, and more. It allows developers to write queries using a familiar syntax and work with data as objects, regardless of the underlying data source.

A LINQ query operation consists of three parts:

1. Obtaining the data source: The data source is the collection or data structure from which the data will be retrieved. It can be an array, a database table, an XML document, or any other object that implements the `IEnumerable<T>` interface.

2. Creating the query: The query is created using query expressions, which are similar to SQL statements. Query expressions define what data to retrieve, how to filter and transform it, and any sorting or grouping operations to be applied. The query expression is assigned to a query variable.

3. Executing the query: The query is executed when it is iterated over, typically using a `foreach` loop. At this point, the query is evaluated, and the actual data is retrieved from the data source and processed according to the query expression.

Here's an example that demonstrates the three parts of a LINQ query operation:

```csharp
class IntroToLINQ
{
    static void Main()
    {
        // 1. Data source
        int[] numbers = new int[7] { 0, 1, 2, 3, 4, 5, 6 };

        // 2. Query creation
        var numQuery =
            from num in numbers
            where (num % 2) == 0
            select num;

        // 3. Query execution
        foreach (int num in numQuery)
        {
            Console.Write("{0,1} ", num);
        }
    }
}
```

In this example, an array of integers serves as the data source. The query is created using the LINQ query expression syntax, where only the even numbers are selected. Finally, the query is executed by iterating over the `numQuery` variable and printing the resulting numbers.

It's important to note that LINQ queries have deferred execution, which means the query itself doesn't retrieve any data until it is iterated over. This allows for more efficient querying and enables scenarios where the data source may be continuously updated. Additionally, queries that perform aggregation functions (e.g., Count, Max, Average) execute immediately because they need to iterate over the data source to calculate the result.

You can force immediate execution and cache query results by calling methods like `ToList()` or `ToArray()` on the query variable.

LINQ provides a powerful and unified approach to working with data, making it easier for developers to query and manipulate data from different sources using a single language syntax.

## [Basic LINQ Query Operators](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/standard-query-operators-overview)

This article provides an overview of the standard query operators in C# and LINQ (Language-Integrated Query). The standard query operators are methods that form the LINQ pattern and operate on sequences, which are objects implementing the IEnumerable<T> or IQueryable<T> interfaces. These operators enable various query capabilities such as filtering, projection, aggregation, sorting, and more.

There are two sets of standard query operators: one for IEnumerable<T> and another for IQueryable<T>. They are defined as static extension methods of the Enumerable and Queryable classes, respectively. These operators can be called using either static or instance method syntax.

In addition to the standard query operators for IEnumerable<T> and IQueryable<T>, there are also methods for non-parameterized collections, such as Cast<TResult> and OfType<TResult>, which allow non-generic collections to be queried using LINQ.

The timing of query execution varies depending on whether the operators return a singleton value or a sequence of values. Methods returning a singleton value execute immediately, while methods returning a sequence defer execution and return an enumerable object.

For in-memory collections (IEnumerable<T>), the enumerable object captures the arguments passed to the method, and the query operator's logic is employed when the object is enumerated. For IQueryable<T>, the query operators build an expression tree representing the query, and the processing is handled by the source IQueryable<T> object.

Multiple query methods can be chained together to create complex queries in a single expression.

The article includes code examples demonstrating the usage of standard query operators to obtain information about a sequence. It covers various aspects such as query expression syntax, filtering, ordering, grouping, joining, and projections.

Additionally, the article mentions that developers can extend the standard query operators by creating domain-specific methods or custom implementations to enhance query capabilities.

Overall, this article serves as a comprehensive introduction to the standard query operators in C# and LINQ, providing developers with essential knowledge to work with LINQ efficiently.

## [Walkthrough Writing LINQ Queries in C#](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/walkthrough-writing-queries-linq)

