# Application Export

The following are steps required to use the frontendcreator-export repository to host files exported from FrontEnd Creator. 

Before you begin, it is important that you have an application ready to export from **FrontEnd Creator**. This is accomplished by creating all the commensurate screens and then defining a navigation for them using the Navigation Builder. It is from the Navigation Builder that you export your application.

1. Clone the GitHub repository: https://github.com/mattduffield/frontendcreator-export.git
2. Run: 'npm install'
3. Export the application using the Navigation Builder export button. (You may need to allow the browser to download the generated .zip file)
4. Extract the .zip file from your download folder.
5. Copy and past the scr folder into the root of the project you just cloned.
6. Choose ‘merge’ as the option for placing the files into the existing project.
7. In the main.js file, uncomment the `.feature('resources');` line of code and remove the preceding semicolon (;) from the line above.
8. If the app you exported is using a shell, change the
 `aurelia.start().then(() => aurelia.setRoot());` to
 `aurelia.start().then(() => aurelia.setRoot('<name of shell>'));`
9. Copy any assets, custom elements, favicon to the corresponding folder.
10. For any assets that need to be in the scripts folder, add each to the 'copyFiles' section of the aurelia.json file under the aurelia_project folder.
11. Update the `resources/index.js` file to include any custom elements, etc. you added.
12. In the shell.html, add `require` tags for all of the styles in the styles folder.
13. Run `au run` and test the web application.

Congratulations, you now have the ability to self host your application!

[ <- Previous ](navigation-builder) | [ Home ](home) | [ Next -> ](template-builder)
