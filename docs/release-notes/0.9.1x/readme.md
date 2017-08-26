# Release Notes

## 1.0.0.x Versions

### 1.0.0.4-beta
- Renaming a file (Ctrl|Cmd + Shift + S) had the wrong file path. It has been corrected to use '/'
- Saving a file made the preview pane hidden but the area was still visible. It has been corrected to no longer hide the preview pane unless it is a new file
- Loading a file made the preview pane hidden but the area was still visible. It has been corrected to no longer hide the preview pane
- In the editor, all HTML files were considered dirty once we tab over to the designer. It has been corrected to ignoring formatting changes and only focus on user changes
- The navigation panel was always refreshing whenever a user saved a file. This no longer happens except for new files and projects
- Support for experimental decorators is turned on by default in the Monaco Editor
- DOM tree had an issue when trying to build selector paths to custom elements that were used both inside and outside of the designer surface. It has been corrected
- The navigation panel now supports exploding the tree to the actual folder for the given file you are working on. This only really is needed when refreshing the browser when you have a loaded file
- The navigation panel now supports highlighting the loaded file in the tree. This is working when you are managing your projects and files and is now working for the editor
- We now have our `Home` route. It will be possible to pin projects to the `Home` route to quick launch them in another tab

### 1.0.0.3-beta
- Now using the Monaco Editor (VS Code editor)
- Several bug fixes related to porting from Ace Editor to Monaco Editor
- Ace Editor custom element has been removed.

### 1.0.0.2-beta
- Now using REST API for Blob Storage. Cold start is much faster now
- Project tree now refreshes when creating a new project
- Project tree now refreshes when creating a new file
- Project tree now provides an icon for all mime-types. It defaults to ones that are not natively supported
- Application now supports Drag-n-Drop from the desktop
- Application now provides a preview for image mime-types
- Application now supports downloading projects containing both text and no-text file types

### 1.0.0.1-beta
- Many bug fixes with the designer and toolboxes
- Support for Adding External Resources (you can do this by using the context-menu on a index.html file)
- Support for Configure Router (you can do this on any *.js file)
- Support for Adding Linked Files (you can do this by using the context-menu at the project root folder)
- This is still very experimental and needs to have support for deleting referenced files as well as consecutive linking of files
- Support for Adding View/ViewModel files (you can do this by using the context-menu at the project root folder)


## 0.9.1x Versions

### 0.9.17
- Added a "Settings" menu item which contains all advanced items
- Both levels of the menu system collapse properly now
- Auth0 security/login now supports most recently used route. This means after a timeout, it will redirect you to the last recently used route
- Issue #12 has been corrected
- Issue #5 has been corrected

### 0.9.16

- Created new Markdown custom element. It will be used for all documentation. A new Markdown editor will be created to allow you to manage your documentation as well as export the markdown or HTML
- Added filter capability to IconDropdown custom element to make it easier to find icons
- Added ListView and ListViewItem custom element to make allow for multiple views of a given set of data
- Fixed bug with the Bootstrap filter in the designer
- Toolbox, Bootstrap, Components now use the ListView custom element to provide different sizing in the designer
- Enhanced the Navigation Menu on the left to collapse whenever you click outside of the Navigation Menu area

### 0.9.15

- All tutorials and documents have been updated to the latest UI. The tutorials have videos so that you can pause and continue
- Application now uses Auth0 for authentication
- Saving in the designer triggers the Preview tab to refresh
- Dialogs now can use the `classBuilder` function to support dependency injection of referenced Scripts
- Fixed issue with Entity Builder using incorrect input types for Default Element 
- Entity Builder when generating radio buttons in the designer did not create unique names when used under collections
- Entity Builder when generating radio buttons uses camel case to proper case for labels
- Fixed issue with Dynamic Element not setting the Schema and validations were failing
- Added date validation to validation engine
- Fixed issue with Schema Editor not parsing correctly
- Fixed issue with Validation Summary missing CSS styles
- Fixed HTML formatter when clicking on the HTML tab in the designer. The formatter now tries to put open and closed tags on their own line with the proper indentation
- Fixed HTML formatter when dealing with HTML comments. It no longer tries to indent for the tag
- Fixed issue with vertical sliders in designer when multiple aside and sidebar elements where on the same surface
- Fixed issue with validator not updating errors when only one of many errors was corrected on a given form
- Added application version number to the User Settings dialog

### 0.9.14

- Added Template Builder for creating reusable templates. It has the ability to visualize the templates with dummy data as well as setting the number of records of data to test with.
  - Added keyboard mnemonics for screen:
    - Ctrl|Cmd + S - Save
    - Ctrl|Cmd + Plus - New
    - Ctrl|Cmd + R - Refresh template preview
- Added Export capability at the application level. You use this by defining your routes and hierarchy with the Navigation Builder and then exporting a .zip file that represents all of the assets used for your application. You will be able to self-host the application using the FrontEnd Creator Export repository.
- Added FrontEnd Creator Export repository on GitHub. You use this repository in conjunction with exporting your application for self-hosting.
- Entity Builder has been expanded to support more default element types. These new types work together with the Template Builder for better semantic visualization. 
- Entities tab, in the designer, now allows you to include/exclude fields using a checkbox. You can also reorder fields so that when you drag the Entity on the designer, it injects the correct fields in the correct order.
- Fixed an issue with Scripts failing to load third-party JavaScript libraries. The way to load libraries has changed slightly, so be sure to review the docs on this.
- Fixed an issue with the HTML Formatter when dragging an Entity from the entity tab onto the designer.
- Fixed an issue with the entity tab filter not responding correctly.

### 0.9.13

- Introduced new UI workflow for a easier user experience
- Back button has been completely removed in all screens
- Added shell host for FrontEnd Creator
- Added top level menu in shell
- Removed all screen menu redundancies. They now use the top level menu in the shell
- Added sidebar for all navigation. You can now access this at anytime during your workflow. It has three widths: Wide, Narrow, and Collapsed
- The new sidebar now hosts all of the FrontEnd Creator tools as well as list all projects and screens dynamically
- Added a new home screen (This screen will be used to pin common work and to launch applications for review)
- Added keyboard mnemonics for common actions using FrontEnd Creator. They are as follows:
  - Ctrl|Cmd + S - Save
  - Ctrl|Cmd + Up arrow - Move a selected element in the designer up
  - Ctrl|Cmd + Down arrow - Move a selected element in the designer down
  - Ctrl|Cmd + Keypad Plus - Creates a new record
  - Ctrl|Cmd + Keypad Minus - Removes a selected element in the designer
  - Ctrl|Cmd + E - Export from the designer
  - Ctrl|Cmd + O - Preview from the designer in a new browser tab
  - Ctrl|Cmd + S - Save
  - Ctrl|Cmd + F1 - Toggle the sidebar
  - Ctrl|Cmd + F2 - Toggle the left panel in the designer or other tools
  - Ctrl|Cmd + F3 - Toggle the right panel in the designer or other tools
- Added ability to tag Projects
- Added ability to tag Screens
- Menu Builder as been renamed to Navigation Builder. It now behaves more like the Aurelia Router. It is hierarchical to represent menu structures easier but is flattened at runtime for route creation
- Multi-Lingual has been renamed to Translation Builder to try to be more consistent with the other tools available in FrontEnd Creator
- Fixed bug when saving in any tool screen from the JSON tab. Previously, you had to switch back to the Form tab to get your changes to persist

### 0.9.12

- Added menu builder. This tool generates an array of data that can be used in any type of menu you like. You simply bind to the data and then render it out as you like. It supports a custom display, along with an icon, and href for navigating. You can navigate to existing screens across all of your projects

### 0.9.11

- Added multi custom element support. Please refer to the documentation for more information

### 0.9.10

- Added custom element support in designer. Please refer to the documentation for more information
- Added caching via data-service to all views within FrontEnd Creator
- Refactored Scripts loading in a screen to be in its own service
- Refactored Styles loading in a screen to be in its own service
- Refactored Language Mapping loading in a screen to be in its own service
- Added Screen ID to screen dialog for quick reference
- Corrected/Fixed bug with Firefox and script loading
- Corrected/Fixed bug in designer after dragging panels; standard drag and drop failed to work
- Corrected/Fixed bug with confirm delete dialog to display prompt message correctly