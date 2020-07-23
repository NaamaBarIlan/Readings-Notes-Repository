# EF Relationships & Advanced APIs

### Reading List:

##### [Routing within MVC](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)
##### [Routing within Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing?view=aspnetcore-3.1)

---

#### ASP.NET MVC Routing

*  The ASP.NET Routing module is responsible for mapping incoming browser requests to particular MVC controller actions. 

* When you create a new ASP.NET MVC application, the application is already configured to use ASP.NET Routing. 

* ASP.NET Routing is setup in two places:

	1. ASP.NET Routing is enabled in your application's Web configuration file (Web.config file). There are four sections in the configuration file that are relevant to routing: 
		* The system.web.httpModules section
		* The system.web.httpHandlers section 
		* The system.webserver.modules section
		* The system.webserver.handlers section 
		
		Be careful not to delete these sections because without these sections routing will no longer work.
	2. A route table is created in the application's Global.asax file. The Global.asax file is a special file that contains event handlers for ASP.NET application lifecycle events. The route table is created during the Application Start event.

* **The Default Route Table** - contains a single route (named Default). The Default route maps the first segment of a URL to a controller name, the second segment of a URL to a controller action, and the third segment to a parameter named id.

	If you enter the following URL into your web browser's address bar:

	`/Home/Index/3`

	The Default route maps this URL to the following parameters:

	**controller** = Home

	**action** = Index

	**id** = 3

	When you request the URL /Home/Index/3, the following code is executed:

	`HomeController.Index(3)`

--- 

#### ASP.NET Core Routing

* Routing is responsible for matching incoming HTTP requests and dispatching those requests to the app's executable endpoints. 

* Endpoints are defined in the app and configured when the app starts. 

* The endpoint matching process can extract values from the request's URL and provide those values for request processing. 

* Using endpoint information from the app, routing is also able to generate URLs that map to endpoints.

* All ASP.NET Core templates include routing in the generated code. Routing is registered in the middleware pipeline in `Startup.Configure`.

* The routing system builds on top of the middleware pipeline by adding the powerful endpoint concept. Endpoints represent units of the app's functionality that are distinct from each other in terms of routing, authorization, and any number of ASP.NET Core's systems.
