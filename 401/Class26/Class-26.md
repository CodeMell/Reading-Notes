# Intro to MVC

[Azure Dev Ops](https://docs.microsoft.com/en-us/azure/devops/?view=azure-devops)

[MVC Basics](https://www.c-sharpcorner.com/article/learn-basics-of-mvc-architecture/)


MVC is a design pattern that separates an application into three distinct components: Model, View, and Controller.

- **Model**: Represents application objects, their properties, and methods.
- **View**: Defines the user interface (UI) using HTML controls. Utilizes Razor Engine for rendering.
- **Controller**: Handles user requests, retrieves data from the Model, and loads appropriate Views.

## Key Differences between ASP.NET Web and MVC

1. **UI and Logic Coupling**:
   - ASP.NET Web: UI and action logic are tightly coupled in code-behind files.
   - MVC: Views handle UI, while user actions are defined in Controllers, promoting loose coupling.

2. **Action-based Architecture**:
   - ASP.NET Web: View-based architecture, not highly efficient for action-based requirements.
   - MVC: Action-based architecture; Views are displayed based on user actions, leading to organized code.

3. **View State**:
   - ASP.NET Web: Uses View State to maintain page state, resulting in heavier pages and inefficient server trips.
   - MVC: Doesn't utilize View State, eliminating this source of inefficiency.

4. **Page Life Cycle**:
   - ASP.NET Web: Follows a full page life cycle for each request, leading to slower response times.
   - MVC: Lacks a page life cycle; Controllers process requests, improving response times.

5. **Testing**:
   - ASP.NET Web: Testing is challenging due to tight coupling of UI and business logic.
   - MVC: Separation of Models, Views, and Controllers enhances test-driven development.

## ASP.NET MVC Advantages

- **Clean Architecture**: MVC divides application into three layers: Model, View, and Controller.
- **Reusability**: Built on top of ASP.NET, MVC logic can be reused across different platforms.
- **Team Collaboration**: Different team members can work on distinct MVC components.
- **Scalability**: Suitable for both light-weight and large-scale applications.

## Selecting the Right Framework

- **ASP.NET Web**: Suitable for RAD models and small-scale applications.
- **ASP.NET MVC**: Ideal for large teams, controlled maintenance, and both small and large-scale applications.

Remember, MVC enhances application development efficiency, separation of concerns, and flexibility in adapting to varying project needs.



[Tag Helpers](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/tag-helpers/intro?view=aspnetcore-2.1)

# Tag Helpers in ASP.NET Core

Tag Helpers in ASP.NET Core allow server-side code to generate and render HTML elements in Razor files. They provide an HTML-friendly development experience and reduce the need for explicit transitions between HTML and C#.

## What are Tag Helpers?

Tag Helpers enable server-side code to create and render HTML elements. They offer an alternative to HTML Helpers and attach to HTML elements in Razor views. They're authored in C# and target HTML elements based on element name, attribute name, or parent tag. Unlike HTML Helpers, Tag Helpers don't replace HTML tags entirely, and both approaches can be used together.

## Benefits of Tag Helpers

1. **HTML-Friendly Development**:
   - Tag Helper syntax closely resembles standard HTML, making it familiar for front-end designers.
   - HTML/CSS/JavaScript experts can work with Razor views without learning extensive C# syntax.

2. **Rich IntelliSense Environment**:
   - Tag Helpers provide a more intuitive development experience than HTML Helpers.
   - IntelliSense support makes it easy to create HTML and Razor markup, enhancing productivity.

3. **Robustness and Maintainability**:
   - Tag Helpers offer automated functionality that improves code reliability.
   - Built-in Tag Helpers like ImageTagHelper automatically handle tasks such as versioning images.

4. **Server-Side Enhancement**:
   - Tag Helpers enhance client experiences by generating dynamic content on the server.
   - For instance, ImageTagHelper ensures clients receive up-to-date images through automatic versioning.

## Managing Tag Helper Scope

- **@addTagHelper**: This directive makes Tag Helpers available to views.
  - Wildcard syntax ("*") imports all Tag Helpers from a specified assembly.
  - Scoped Tag Helpers can be introduced through specific view files for fine-grained control.

- **@removeTagHelper**: Removes previously added Tag Helpers from views.
  - Works similarly to `@addTagHelper`, but removes the specified Tag Helpers.
  - Can be used to limit the scope of Tag Helpers in specific folders or views.

- **@tagHelperPrefix**: Sets a tag prefix to make Tag Helper usage explicit.
  - Tag Helpers with the specified prefix are enabled for elements using that prefix.
  - Provides control over which elements are affected by Tag Helpers.

## Self-Closing Tag Helpers

- Some Tag Helpers can be self-closing, while others are not designed for it.
- Using a non-self-closing Tag Helper as self-closing can lead to suppressed output.
- Self-closing a Tag Helper results in a self-closing tag in the rendered output.

## Limitations and Differences

- Tag Helpers don't support C# code within attributes or tag declarations.
- Tag Helper syntax provides cleaner and more readable markup compared to HTML Helpers.
- Tag Helpers are distinct from ASP.NET Web Server Controls with different lifecycles and scopes.

## Conclusion

Tag Helpers in ASP.NET Core offer an HTML-friendly way to generate and render HTML elements using server-side code. They provide benefits such as a more intuitive development experience, automated functionality, and improved code maintainability. While they don't replace HTML Helpers or Web Server Controls, they offer a valuable addition to the toolkit for creating robust and dynamic web applications.

For more detailed information and examples, refer to the original article.


[Bootstrap](https://getbootstrap.com/)

[1 Hour tutorial Bootstrap](https://scrimba.com/g/gbootstrap4)