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

[Bootstrap](https://getbootstrap.com/)

[1 Hour tutorial Bootstrap](https://scrimba.com/g/gbootstrap4)