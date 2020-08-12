# Layouts

### Reading List:

##### [View Layouts](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/layout?view=aspnetcore-2.1)
##### [Partial Views](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/partial?view=aspnetcore-2.1)
##### [View Models](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-2.2)
##### [Tag Helpers](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/tag-helpers/intro?view=aspnetcore-2.1)
##### [Tag Helpers with Forms](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/working-with-forms?view=aspnetcore-2.1)

---

### View Layouts
* Most web apps have a common layout that provides the user with a consistent experience as they navigate from page to page. The layout typically includes common user interface elements such as the app header, navigation or menu elements, and footer.
* Common HTML structures such as scripts and stylesheets are also frequently used by many pages within an app. 
* All of these shared elements may be defined in a layout file, which can then be referenced by any view used within the app. Layouts reduce duplicate code in views.
* By convention, the default layout for an ASP.NET Core app is named _Layout.cshtml. 
* The layout defines a top level template for views in the app. 
* Apps don't require a layout. 
* Apps can define more than one layout, with different views specifying different layouts.

### Partial Views

* A partial view is a Razor markup file (.cshtml) that renders HTML output within another markup file's rendered output.
* The term partial view is used when developing either an MVC app, where markup files are called views, or a Razor Pages app, where markup files are called pages. 
* Partial views are an effective way to:
	* Break up large markup files into smaller components.
	* Reduce the duplication of common markup content across markup files.
* Partial views shouldn't be used to maintain common layout elements. Common layout elements should be specified in _Layout.cshtml files.
* Where complex rendering logic or code execution is required to render the markup, use a view component instead of a partial view.

### View Models
* In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction. 
* A view is an HTML template with embedded Razor markup. Razor markup is code that interacts with HTML markup to produce a webpage that's sent to the client.
* In ASP.NET Core MVC, views are .cshtml files that use the C# programming language in Razor markup. Usually, view files are grouped into folders named for each of the app's controllers. 
* Views help to establish separation of concerns within an MVC app by separating the user interface markup from other parts of the app. 
* Views that are specific to a controller are created in the Views/[ControllerName] folder. Views that are shared among controllers are placed in the Views/Shared folder.

### Tag Helpers

* Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files.
* There are many built-in Tag Helpers for common tasks - such as creating forms, links, loading assets and more - and even more available in public GitHub repositories and as NuGet packages. 
*  Tag Helpers are authored in C#, and they target HTML elements based on element name, attribute name, or parent tag. 
* Tag Helpers don't replace HTML Helpers and there's not a Tag Helper for each HTML Helper.
