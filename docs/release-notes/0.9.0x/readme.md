# 0.9.0x Release Notes

### 0.9.09

- Projects, Screens, Styles, Scripts, Entity Builder all have subtle cursor and background hover changes
- Added Radio option to Entity Builder
- Added Select option to Entity Builder
- Added Market Place
- Added ability to download from Market Place
- Added ability to upload to Market Place
- Added ability to set user avatar. This is used in Market Place and all screens
- Created Multilingual Builder. This allows you to provide support for multiple languages using a simple convention. Please refer to the documentation for more information. FrontEnd Creator now supports: English, French, German, Italian, Portuguese, and Spanish. Please let me know if they translations are not correct
- User Settings dialog now allows you to set an avatar by clicking on the avatar icon in the top right of the dialog. Please refer to the documentation for more information

### 0.9.08

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

### 0.9.07

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

### 0.9.06

- The scripts tab in the designer has been removed and added as a multi-select to Settings
- The selected scripts footer in the designer has been removed in favor of the multi-select under the Settings
- Added a new Styles editor, this allows for creating your own CSS classes
- Added styles multi-select in the designer under the Settings
- Added a feedback link from the User button dialog
- Added a feedback dialog that stores user feedback to backend
- In the designer, the Toolbox, Bootstrap (optional), and Components tabs become disabled when an item is selected in the designer
- In the designer, the Properties Grid is now cleared out when no item is selected

### 0.9.05

- Added a new three part tutorial on building a container with sliding panels. It is the same style in which the designer has been built. This tutorial showcases some of the powerful features you can do with Aurelia and composition. It also demonstrates how you can inline styles in your own screens and components.
- Updated the existing tutorials to reflect some changes with classes that are provided in the Property Grid for autocomplete. They mainly focus around Flexbox and Layout classes.
- Added the ability to perform dependency injection on Scripts. You can now create ES6 Classes and those can be marked up with the decorator '@inject(...)'. These classes are save along with your screens and when a screen is loaded, it checks to see if any scripts are needed. When a script is loaded, it first injects any dependencies before returning you a new object.

### 0.9.04

- Refactored multi-selector custom element for designer
- Added Flexbox CSS classes
- Added Layout CSS classes
- Adjusted all routing to no longer require unique screen names. Now based on unique ID