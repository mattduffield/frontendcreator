## 1.0.0.x Versions

### 1.0.0.7-beta
- Added ability to commit to GitHub
- Added ability to commit to Bitbucket
- Added ability to provide your own commit comment
- GitHub/Bitbucket repo is created using the same name as your project
- Added ability to select default source control repository (GitHub or Bitbucket)
- Added ability to choose what protocol to use (HTTP or HTTPS) when previewing your app
- Added ability to choose how you wish to navigate between files (Auto-save or Prompt)
- Fixed issue when selecting an already opened tab from the tree to highlight it properly
- Fixed issue when multiple tabs were open they always reflected the name of the currently opened record

### 1.0.0.6-beta
- Added ability to clone projects from Market Place
- Added ability to export file(s) from Market Place
- Added Syncfusion sample project to Market Place
- Added KendoUI sample project to Market Place
- Added Contact Manager sample project to Market Place
- Added tabs for each open file
- Fixed context menu from display when not over an item
- Fixed linked files recursive bug when adding new files

### 1.0.0.5-beta
- Added Sign up link to Auth0
- Upgraded to the latest version of Auth0 API
- Upgraded to PushState
- Fixed file extension MIME type evaluation to be case insensitive. (Thanks @johntom for finding this!)
- Added support for Gravatar API. It now findsyour gravatar just like Auth0
- Adding new files now remembers the location you were for the previous file
- Clicking on a folder will automatically provide the file path so that it is easier to save the file in the correct location
- Added ability to add new file from project navigation panel
- Fixed issue when switching between Designer tab and HTML tab and the Editor would become hidden
- Turned on Code Folding as a default setting for Editor
- Added a close button to the Preview pane. It now remembers where it was so that when you turn on preview, it will return to the same location. (Thanks @jawa-the-hutt for the suggestion!)
- Added a project-manifest.json to all new projects
- Updated the Manage Linked Files workflow
- Saving any file that is linked now saves all reference linked files
- Deleting any file that is a source for reference linked files now shows a dialog with all of the files in question
- Managed Linked Files can now add/remove links via a secondary dialog
- Added ability to edit markdown files and Preview
- Markdown Preview allows for multiple styles for your code snippets
- Markdown Preview supports images
- Markdown Preview supports YouTube and Vimeo videos
- New sample application Contact Manager
- All screens now support keyboard mnemonics. The mnemonics are consistent and the same across all screens:
  **Projects Panel**
  - Ctrl|Cmd + Dash - Add New Project
  - Ctrl|Cmd + Equal Sign - Add New File 
  - Ctrl|Cmd + Forward Slash - Clone selected files
  - Ctrl|Cmd + Delete|Backspace - Remove selected files
  - Ctrl|Cmd + Z - Configure Router (Only on a selected .js file)
  - Ctrl|Cmd + M - Manage External Resources (Only on a selected index.html file)
  - Ctrl|Cmd + R - Refresh
  - Ctrl|Cmd + E - Toggle Tree Expansion 
  - Ctrl|Cmd + D - Download selected files
  **Project Panel with Editor (file loaded)**
  - Ctrl|Cmd + Equal Sign - Add New File 
  - Ctrl|Cmd + S - Save
  - Ctrl|Cmd + Shift + S - Save As
  - Ctrl|Cmd + E - Toggle Tree Expansion 
  - Ctrl|Cmd + Shift + 6 - Toggle Preview
  - Ctrl|Cmd + Shift + 7 - Preview In Tab
  **Project Panel with Designer (.html file loaded)**
  - Ctrl|Cmd + Shift + 1 - Show Toolbox
  - Ctrl|Cmd + Shift + 2 - Show Custom Elements
  - Ctrl|Cmd + Shift + 3 - Show Bootstrap
  - Ctrl|Cmd + Shift + 4 - Show Entities
  - Ctrl|Cmd + Shift + 5 - Toggle DOM Tree Visibility
  - Ctrl|Cmd + Shift + 6 - Toggle Preview
  - Ctrl|Cmd + Shift + 7 - Preview In Tab
  - Ctrl|Cmd + Up Arrow - Move selected element up
  - Ctrl|Cmd + Down Arrow - Move selected element down
  - Ctrl|Cmd + Forward Slash - Clone selected element
  - Ctrl|Cmd + Delete|Backspace - Remove selected element
  - Ctrl|Cmd + S - Save


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
