# Bootstarp & MVC

### Reading List:

##### [Azure Dev Ops](https://docs.microsoft.com/en-us/azure/devops/?view=azure-devops)
##### [1 Hour tutorial Bootstrap](https://scrimba.com/g/gbootstrap4)
##### [Build sites with Bootstrap]()
##### [Bootstrap](https://getbootstrap.com/)

---

### Azure DevOps

Azure DevOps provides developer services to support teams to plan work, collaborate on code development, and build and deploy applications.

#### Included Services:

* *Azure Repos* - provides Git repositories or Team Foundation Version Control (TFVC) for source control of code
* *Azure Pipelines* -  provides build and release services to support continuous integration and delivery of apps
* *Azure Boards* - delivers a suite of Agile tools to support planning and tracking work, code defects, and issues using Kanban and Scrum methods
* *Azure Test Plans* - provides several tools to test apps, including manual/exploratory testing and continuous testing
* *Azure Artifacts* -  allows teams to share Maven, npm, and NuGet packages from public and private sources and integrate package sharing into CI/CD pipelines
* Customizable team dashboards with configurable widgets to share information, progress, and trends
* Built-in wikis for sharing information
* Configurable notifications

Azure DevOps includes extensions and integrating with other popular services, such as: Campfire, Slack, Trello, UserVoice, and more.

### Bootstrap

Bootstrap is a framework for building responsive, mobile-first sites. It is a helpful tool for adding a simple front end to a site. 

This front end framework uses a responsive grid of flexible, collapsible components. 

The Bootstrap 4 tutorials cover the following topics:
* Responsive Grid Systems
	Sample code:
    ```<body>
        
        <div class="container" style="margin-top:30px;">
            <h5>Basic Columns</h5>
            <div class="row">
                <div class="col">column</div>
                <div class="col">column</div>
                <div class="col">column</div>
            </div>
        </div>
        
        <div class="container" style="margin-top:30px;">
            <h5>Set Sizes</h5>
            <div class="row">
                <div class="col-4">column</div>
                <div class="col-6">column</div>
                <div class="col-2">column</div>
            </div>
        </div>
        
        <div class="container" style="margin-top:30px;">
            <h5>Breakpoints</h5>
            <div class="row">
                <div class="col-sm">column</div>
                <div class="col-sm">column</div>
            </div>
        </div>
        
        <div class="container" style="margin-top:30px;">
            <h5>Set Sizes and Breakpoints</h5>
            <div class="row">
                <div class="col-sm-4">column</div>
                <div class="col-sm-6">column</div>
                <div class="col-sm-2">column</div>
            </div>
        </div>
        
        <div class="container" style="margin-top:30px;">
            <h5>No Gutters</h5>
            <div class="row no-gutters">
                <div class="col">column</div>
                <div class="col">column</div>
            </div>
        </div>
        
        <div class="container" style="margin-top:30px;">
            <h5>Offsetting Columns</h5>
            <div class="row">
                <div class="col-sm-6">column</div>
                <div class="col-sm-3 offset-sm-3">column</div>
            </div>
        </div>

    </body>```
    
* Responsive Navbars
    Sample code:
    
    ```<body>
        
        <nav class="navbar navbar-light bg-light navbar-expand-lg fixed-top">
            <a href="#" class="navbar-brand">My Website</a>
            <button class="navbar-toggler" data-toggle="collapse" data-target="#navbarCollapse">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarCollapse">
                <ul class="navbar-nav ml-auto">
                    <li class="navbar-item">
                        <a href="#" class="nav-link">Homepage</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nav-link">Blog</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nav-link">About Me</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nav-link">Contact</a>
                    </li>
                </ul>
            </div>
        </nav>
    </body>```

* Modals
  Sample Code:

  ```<body>
        
        <button class="btn btn-primary" data-toggle="modal" data-target="#myModal">Launch Modal</button>
        
        <div class="modal fade" id="myModal">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Hello World</h5>
                        <button type="button" class="close" data-dismiss="modal">
                            <span>&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <p>Lorem ipsum dolor</p>
                    </div>
                    <div class="modal-footer">
                        <button class="btn btn-primary" data-dismiss="modal">Cancel</button>
                    </div>
                </div>
            </div>
        </div>

    </body>```

* Forms 
  Sample Code:
   
   ```<body>
        
        <div class="container" style="margin-top:20px;">
            
            <form>
                <div class="form-group row">
                    <label class="col-sm-3 col-form-label" for="email">Email Address</label>
                    <div class="col-sm-9">
                        <input type="text" class="form-control" id="email">
                    </div>
                </div>
                
                <div class="form-group row">
                    <label class="col-sm-3 col-form-label" for="password">Password</label>
                    <div class="col-sm-9">
                        <input type="password" class="form-control" id="password">
                    </div>
                </div>
                
                <div class="row">
                    <div class="col-sm-9 offset-sm-3">
                        <button type="submit" class="btn btn-primary">Login Now</button>
                    </div>
                </div>
                
            </form
            
        </div>

    </body>```

* List Groups 
  Sample Code:

  ```<body>
        
        <div class="container" style="margin-top:30px">
            
            <div class="list-group">
                <a href="#" class="list-group-item list-group-item-action">
                    Homepage
                </a>
                <a href="#" class="list-group-item list-group-item-action d-flex justify-content-between align-items-center">
                    Notifications
                    <span class="badge badge-primary badge-pill">3</span>
                </a>
                <a href="#" class="list-group-item list-group-item-action">
                    Blog
                </a>
                <a href="#" class="list-group-item list-group-item-action">
                    Contact
                </a>
            </div>
            
        </div>
    </body>```

* Cards
* Tables
* Alerts
* Navigation Options
