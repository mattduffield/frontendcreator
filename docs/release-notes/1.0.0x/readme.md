## 1.0.0.x Versions

### 1.0.0.1-RC
- This is a breaking release!
- New file tree
- New routing infrastructure
- New Project wizard
- Open Project dialog
- All Git interactions now happen in Azure Functions
- New File Uploader 
- Re-designed Monaco Editor


### 1.0.0.19-beta
- Fixed Market Place close tab button not responding
- Fixed issue #21 where creation of an Entity was not working
- Fixed issue #22 the delete prompt for a project now includes the project name
- Fixed issue #23 deleting entities did not work. This fix corrected both deleting entities as well as cloning
- Fixed issue #24 managing entities should now work and was fixed by #21 and #23
- Fixed issue #25 typo in the guide book. The text has been corrected
- Confirm delete dialog in the Project panel, now lists all of the files that have been selected for delete

### 1.0.0.18-beta
- Updated all CORS settings for Blob Storage to support HTTPS
- Updated all user settings for Preview to now use HTTPS
- Fixed bug with tab not updating cache when switching or loading a new file

### 1.0.0.17-beta
- Added support for caching current cursor location for open tab
- Added support for restoring cached cursor location after opening a tab
- Added support for when clicking the close button on the tab so that it opens a save dialog if dirty
- Added dirty icon to the current tab when the editor is dirty
- Fixed bug when logging out not clearing cached tabs or projects
- Fixed bug in Market Place context menu showing Unload Project menu item
- Fixed bug in Save Dialog when editor is dirty and cached information was assigned to the wrong tab

### 1.0.0.16-beta
- Added open project dialog
- Added unload project to context menu
- Added caching support for open projects
- Added caching support for open tabs
- Added context menu for tabs including: Close, Close Others, Close to the Right, and Close All
- Added preview URL timestamp for browser cache busting
- Added splitter between navigation panel and editor
- Added caching support for splitter width
- Added Phaser as a new project template
- Fixed bug with navigation panel when adding a new file and partially typing a name and hitting the `ESCAPE` key. Now the entry is ignored instead of creating a partially named file
- Fixed CSS styling for HTML designer top right buttons

### 1.0.0.15-beta
- Updated Monaco Editor to use worker proxy
- Added support for Angular 4x development
- Added `Angular + TypeScript` project type
- Added `Angular Heros` sample app to the Market Place
- Refactored preview iFrame logic
- Fixed bug with Preview tab remaining blank

### 1.0.0.14-beta
- Added `React Simple Spa` sample app to Market Place
- Updated React project template
- Updated Preview iFrame to only load when open
- Updated User Settings dialog for more data
- Updated visible-tracker custom attribute to publish visible event for any element

### 1.0.0.13-beta
- Added support for React development
- Added `React + Babel` project type
- Added more mime types for editor
- Fixed timeout navigation issue with Auth0

### 1.0.0.12-beta
- Added custom tasks to build automation for production
- More work on Auth0 silent renewal of tokens
- Fixed issue with designer surface selector holding incorrect reference

### 1.0.0.11-beta
- Added Auth0 capability for silent renewal of token
- Added support for TypeScript development
- Added Skeleton TypeScript sample to Market Place
- Added editor support for TypeScript mimetype
- Added dropdown button for New Project
- Added `Aurelia + Babel` project type
- Added `Aurelia + TypeScript` project type
- Fixed issue with copy/paste operation holding on to old href
- Fixed issue with copy/paste operation holding on to old container
- Fixed issue with export operation not working in Projects
- Fixed context menu not showing up after opening and closing a file

### 1.0.0.10-beta
- Added a link to the image preview in the designer. This allows you to launch your images for preview in a separate browser tab
- Added a copy to clipboard button to the image preview in the designer. This is just a shortcut for grabbing the URL of the image for use in your applications or sharing
- Fixed issue with the navigation buttons when deleting a file; both tabs and the tree items were not being removed
- Fixed Market Place where the `clone` button was no longer visible
- Fixed Market Place where the `download` button was no longer visible
- Fixed Market Place where the `preview` button was no longer visible
- Fixed Market Place where the `play` button was no longer visible
- Fixed the `Toggle Expand` button to be fully recursive in the Navigation Tree


### 1.0.0.9-beta
- Rewrote navigation tree to behave more like the tree in VSCode. This was by far one of the biggest requests and confusions when using FrontEnd Creator. This tree has all the behavior that you would expect, e.g. Copy, Paste, Delete, etc.
- Removed the dual mode in the editor. Previously you were either in project mode or editor mode. This constraint is no longer necessary.
- Added the ability to create folders in the tree
- Added the ability to create files in the tree
- All context menu actions in the navigation tree require no refresh. The navigation buttons above the tree will still for refresh for some actions
- Added better contextual support for Add Viiew/View Model feature. You now have the ability to do it from any folder in your project and it correctly sets the path for you
- Clicking on a tab now expands the tree to show where the file is located in the tree
- Fixed issue when tree height was calculated incorrectly and did not let you see bottom part of tree
- Added auto scroll feature to tree so that when you refresh the tree, if there is a file open, it will auto scroll to the currently open file
- Fixed issue with Firefox not rendering the project name input width correctly

### 1.0.0.8-beta
- Add new automated documenation engine for creation of Markdown files and screenshots
- Fixed CORS issue with Azure Function service for GitHub
- Fixed CORS issue with Azure Function service for Bitbucket
- Fixed JSON property issue for SourceControl property
- Fixed issue with clicking on Editor tabs not working
- Fixed padding issue with .main-header button
- Fixed issue with creating a new Entity and immediately trying to create another. Preview data was still persisted
- Fixed issue with creating a new Templates and immediately trying to create another. Preview data was still persisted
- Fixed issue with creating a new Translations and immediately trying to create another. Preview data was still persisted
- Fixed issue with new Entity containing redundant userId
- Fixed issue with new Templates containing redundant userId
- Fixed issue with new Translations containing redundant userId
- Fixed issue with Editor adding new tab when clicking on custom tools


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
