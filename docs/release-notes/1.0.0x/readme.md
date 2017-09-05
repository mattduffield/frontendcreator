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
