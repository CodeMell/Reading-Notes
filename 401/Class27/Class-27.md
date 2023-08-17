 # MVC Forms

[View Models](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-2.2)

1. **Benefits of Using Views:**
   - Views help establish a separation of concerns (SoC) within an MVC app, making it modular and organized.
   - Different app parts are loosely coupled, allowing updates to views without affecting other components.
   - Testing user interface parts becomes easier due to the separation of views.

2. **Creating a View:**
   - Views specific to a controller are stored in the `Views/[ControllerName]` folder, while shared views are placed in `Views/Shared`.
   - To create a view, add a new `.cshtml` file with the same name as its associated controller action.
   - Razor markup starts with the `@` symbol and allows mixing C# code with HTML.

3. **How Controllers Specify Views:**
   - Views are typically returned from controller actions as a `ViewResult`.
   - Most controllers inherit from `Controller`, which provides the `View` helper method for returning views.
   - The default behavior is to search for a view with the same name as the action method in the corresponding folder.

4. **View Discovery:**
   - The view discovery process determines which view file is used based on the view name.
   - The default behavior searches first in the controller's folder and then in the shared folder.
   - Both implicit and explicit return of views follow the same discovery process.

5. **Passing Data to Views:**
   - Data can be passed to views using various methods:
     - Strongly typed data (viewmodels)
     - Weakly typed data using `ViewData` or `ViewBag`
   - Strongly typed viewmodels provide type safety and are recommended for passing data.

6. **ViewData and ViewBag:**
   - `ViewData` and `ViewBag` are used to pass data between controllers and views.
   - `ViewData` is a dictionary of weakly typed objects, while `ViewBag` provides dynamic properties.
   - `ViewBag` doesn't require explicit casting, but both are error-prone compared to viewmodels.

7. **Dynamic Views:**
   - Views that receive a model instance but don't declare a model type can reference the instance's properties dynamically.
   - This provides flexibility but lacks compile-time checks and IntelliSense.

8. **CSS Isolation:**
   - CSS isolation is a feature that allows CSS styles to be scoped to individual pages, views, and components.
   - Styles are placed in companion `.cshtml.css` files and are bundled during build time.
   - The bundled CSS file is linked in the layout, and styles are isolated using scope identifiers.

9. **CSS Preprocessor Support:**
   - CSS preprocessors like Sass or Less can be integrated with CSS isolation.
   - Preprocessor compilation should occur before CSS isolation during the build process.

10. **CSS Isolation Configuration:**
    - Customizing scope identifier format and changing the base path for static web assets is possible.
    - Automatic bundling can be disabled for more control over the process.

11. **Razor Class Library (RCL) Support:**
    - Isolated styles in a Razor class library are linked using the `_content` path and the package identifier.

[4 Ways to make a form in .NET MVC](https://www.completecsharptutorial.com/asp-net-mvc5/4-ways-to-create-form-in-asp-net-mvc.php)

### 1. Forms - Weakly Typed (Synchronous)

1. In the `Views/Home/Index.cshtml` file, create a simple HTML form using the `form` tag and input elements.
2. The form's `action` attribute should point to an action method in the controller, e.g., `"form1"`.
3. Define the `form1` action method in `HomeController.cs`. It takes parameters for form data and sets `ViewBag` properties.
4. Display the form data in the `Index.cshtml` view using `ViewBag`.

### 2. Forms - Strongly Typed (Synchronous)

1. Define a model class, `StudentModel`, with properties for form fields.
2. In `Views/Home/Index.cshtml`, use the `@model` directive to set the model type.
3. Use `Html.BeginForm` to create a strongly typed form, binding form fields to model properties.
4. Define an action method, `Form2`, in the controller to handle form submissions.
5. Use the model object as a parameter in the `Form2` method and set `ViewBag` properties for display.

### 3. Forms - Strongly Typed AJAX (Asynchronous)

1. Add jQuery Unobtrusive AJAX scripts to the project.
2. In `Views/Home/Index.cshtml`, use `Ajax.BeginForm` to create an asynchronous AJAX form.
3. Specify the action method, controller, HTTP method, and other AJAX options.
4. Define the `Form3` action method in the controller to handle AJAX form submissions.
5. Return content with form data in the `Form3` method, which updates a specific target area on success.

### 4. Pure HTML Forms with AJAX and jQuery

1. In `Views/Home/Index.cshtml`, create an HTML form with input fields and a submit button.
2. Use jQuery to handle the form submission by collecting input values.
3. Create a JavaScript function, e.g., `submit`, to gather form data and send a POST request.
4. Define the `Form4` action method in the controller to handle the POST request.
5. Return JavaScript code that updates an HTML element with the form data.

Each of these methods demonstrates different ways to create forms in ASP.NET MVC, catering to various scenarios and requirements.