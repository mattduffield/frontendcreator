# Navigation Menu

Once you are logged in, you will see the Navigation Menu on the left side of the screen:

![Home](../../assets/images/home-navigation-menu-full.png)

This menu can be partially collapsed, or fully collapsed by clicking on the hamburger button ![Home](../../assets/images/button-hamburger.png) once, or twice respectively. You can also use the keyboard mnemonic `Cmd|Ctrl + F1` to toggle through each width.

The navigation menu is broken up into two sections. The upper section consists of tools to help you with building your web applications. The lower section is below the `Manage Projects` tool. This section is dynamic based on the projects you have created using the `Manage Projects` tool.

## Navigation Menu Contents

#### Styles
The Styles screen is where you are presented with an editor and a list of existing styles for your project. You can perform all actions necessary for managing styles. You author styles using standard CSS syntax.

#### Scripts
The Scripts screen is where you are presented with an editor and a list of existing scripts for your project. You can perform all actions necessary for managing screens. You author scripts using ES6 class syntax.

#### Navigation Builder
The Navigation Builder screen is where you defines routes for your application. It is typically one of the final steps in building your application. The routes you define are standard Aurelia routes. The navigation builder allows you to define a hierarchy with your routes so that you can also use the routes as a menu.

You also have the ability to have labels and placeholder just like the Navigation Menu itself and the dynamic projects.

Finally, it from the Navigation Builder that you are able to `export` your application for self-hosting.

#### Translation Builder
The Translation Builder screen is where you can define multiple translations for you application. You will always have a base translation which all other translations will reference using the `Group With` select element. 

The Translation Builder uses a simple convention. When you select a translation from the Settings tab in the designer, you have the ability to then bind off of it and the translation engine will do the rest provided you have more than one translation available. The parent object you bind off is the `lng` object.

#### Entity Builder
The Entity Builder screen is where you define entity schema. This is used primarily in the desinger when you want to create data forms quickly. The Entity Builder currently supports generating the following types:

* Edit Form - a form with data entry fields
* View Form - a form with view only fields
* Edit Table - a table with data entry fields
* View Table - a table with view only fields

The Entity Builder has special `type` and `default element` values that work with the Template Builder.

#### Template Builder
The Template Builder screen is where you create reusable templates in a quick code and preview manner. It supports a templating syntax that allows you to reference position layout for values the correspond to an entity defined by the Entity Builder. 

The Template Builder is allows you to create advanced screen mockups with very little coding.

#### Market Place
The Market Place screen is where you can upload and download content from other users. It is meant as a place for learning and sharing.

#### Manage Projects
The Manage Projects screen is where you go to create, edit, and delete existing projects.

#### Projects (by name)
These projects will only appear after you have created your first project. You can create as many projects as you like. It is from the individual projects that you are able to lauch a sub-menu showing all of the screens pertaining to that project. In the sub-menu, you can create, edit, and delete existing screens.

