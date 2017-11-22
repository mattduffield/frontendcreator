
# Using Plugins in FrontEnd Creator
FrontEnd Creator comes equipped with only a minimal set of plugins provided by Aurelia. Being able to utilize other existing plugins is fairly easy and only require a few steps to get a plugin bundled properly to be used in your application.

## Bundling
In order to use the `aurelia-dialog` plugin, it is necessary to bundle it so that you can use it in **FrontEnd Creator**. The following steps will walk you through what is necessary to bundle a plugin. We will be using the Aurelia CLI for the bundling process:

1. Install the plugin using the `Aurelia CLI` as follows:
  ```
  au install aurelia-dialog
  ```
2. Next, open the `aurelia.json` file located under the `aurelia_project` folder.
3. Under the `bundles` section of the file, copy and paste the following:
  ```json
  {
    "name": "aurelia-dialog.js",
    "dependencies": [
      {
        "name": "aurelia-dialog",
        "main": "aurelia-dialog",
        "path": "../node_modules/aurelia-dialog/dist/amd",
        "resources": []
      }
    ]
  }        
  ```
4. Save the `aurelia.json` file.
5. In a terminal window, execute the following command:
  ```
  au build --env prod
  ```
6. This should produce the bundle along with the rest of the buildes defined in the `aurelia.json` file.
7. You should now be able to publish `aurelia-dialog.js` to any server you wish for consumption. We will publish the file to the following location: `https://fec.blob.core.windows.net/bundles/aurelia-dialog/1.0.0-rc.2.0.0/aurelia-dialog.js`
8. In the `index.html` file, be sure to include the added bundle in the paths section:
  ```json
  "aurelia-dialog": "https://fec.blob.core.windows.net/bundles/aurelia-dialog/1.0.0-rc.2.0.0/aurelia-dialog"
  ```
9. Notice, that we are not including the `.js` extension since **FrontEnd Creator** uses `RequireJS` as the loader for our files.

10. This will allow you to then add the plugin in your `main.js` file as follows:
  ```javascript
  export function configure(aurelia) {
    aurelia.use
      .standardConfiguration()
      .developmentLogging()
      .plugin('aurelia-dialog');

    aurelia.start().then(a => a.setRoot());
  }
  ```
10. Finally, you are able to reference the newly added plugin in any of our view models like the following:
  ```javascript
  import {DialogService} from 'aurelia-dialog';
  ```
11. You are all set!