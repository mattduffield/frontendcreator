#Release Notes

##0.9.14
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

##0.9.13
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

##0.9.12
- Added menu builder. This tool generates an array of data that can be used in any type of menu you like. You simply bind to the data and then render it out as you like. It supports a custom display, along with an icon, and href for navigating. You can navigate to existing screens across all of your projects

##0.9.11
- Added multi custom element support. Please refer to the documentation for more information

##0.9.10
- Added custom element support in designer. Please refer to the documentation for more information
- Added caching via data-service to all views within FrontEnd Creator
- Refactored Scripts loading in a screen to be in its own service
- Refactored Styles loading in a screen to be in its own service
- Refactored Language Mapping loading in a screen to be in its own service
- Added Screen ID to screen dialog for quick reference
- Corrected/Fixed bug with Firefox and script loading
- Corrected/Fixed bug in designer after dragging panels; standard drag and drop failed to work
- Corrected/Fixed bug with confirm delete dialog to display prompt message correctly

##0.9.9
- Projects, Screens, Styles, Scripts, Entity Builder all have subtle cursor and background hover changes
- Added Radio option to Entity Builder
- Added Select option to Entity Builder
- Added Market Place
- Added ability to download from Market Place
- Added ability to upload to Market Place
- Added ability to set user avatar. This is used in Market Place and all screens
- Created Multilingual Builder. This allows you to provide support for multiple languages using a simple convention. Please refer to the documentation for more information. FrontEnd Creator now supports: English, French, German, Italian, Portuguese, and Spanish. Please let me know if they translations are not correct
- User Settings dialog now allows you to set an avatar by clicking on the avatar icon in the top right of the dialog. Please refer to the documentation for more information

##0.9.8
- Updated Project screen to have Project and Templates (Entity Builder, Scripts, and Styles)
- Updated Entities tree under Entities tab in designer to have color
- Designer, Entity Builder, Scripts, Styles, now all support sliders. Sliders only work when opened
- Added flex-container custom element
- Added dirty screen dialog to ask user if they want to save instead of auto saving. Just in case you want to ignore your changes
- Added DOM tree to designer. This is still very experimental
- All editor screens now use flex-container
- Utilized TaskQueue in order to set focus once a new row has been added. Changes apply to Entity Builder
- Data is now in sync in Entity Builder, Scripts, and Styles when you save a record and then try to reload it from the tree
- If you click Load button in the Entity Builder, Scripts, or Styles, a dirty screen is checked before loading
- If you click New button in the Entity Builder, Scripts, or Styles, a dirty screen is checked before loading

##0.9.7
- In the designer, the Properties Grid is now clear out when a selected item is deleted
- Removed `Save As` button from designer
- Added `Clone` button to individual screen item on the Screens page. Clicking the button launches a dialog window to allow the user to provide new properties
- Added `Preview` button to individual screen item on the Screens page. Click the button opens a new tab for previewing the corresponding screen
- Added implicit save to Back button on the Designer
- Added implicit save to Back button on Scripts editor
- Added implicit save to Back button on Styles editor
- Added new Entity Builder screen
- Updated Designer to support Entities with drag and drop
- Fixed issue with still being able to drag from Components tab when disabled
- Fixed issue with scroll bars always showing (test on Mac) and Toolbox and other tabs were offset
- Added release notes to wiki

##0.9.6
- The scripts tab in the designer has been removed and added as a multi-select to Settings
- The selected scripts footer in the designer has been removed in favor of the multi-select under the Settings
- Added a new Styles editor, this allows for creating your own CSS classes
- Added styles multi-select in the designer under the Settings
- Added a feedback link from the User button dialog
- Added a feedback dialog that stores user feedback to backend
- In the designer, the Toolbox, Bootstrap (optional), and Components tabs become disabled when an item is selected in the designer
- In the designer, the Properties Grid is now cleared out when no item is selected

##0.9.5
- Added a new three part tutorial on building a container with sliding panels. It is the same style in which the designer has been built. This tutorial showcases some of the powerful features you can do with Aurelia and composition. It also demonstrates how you can inline styles in your own screens and components.
- Updated the existing tutorials to reflect some changes with classes that are provided in the Property Grid for autocomplete. They mainly focus around Flexbox and Layout classes.
- Added the ability to perform dependency injection on Scripts. You can now create ES6 Classes and those can be marked up with the decorator '@inject(...)'. These classes are save along with your screens and when a screen is loaded, it checks to see if any scripts are needed. When a script is loaded, it first injects any dependencies before returning you a new object.

##0.9.4
- Refactored multi-selector custom element for designer
- Added Flexbox CSS classes
- Added Layout CSS classes
- Adjusted all routing to no longer require unique screen names. Now based on unique ID