#Form Screen Tutorial

The following are the steps required to use **FrontEnd Creator** to create a simple hello world form with databinding. Here is a screen shot of the layout we are going to build:

![Tutorial Project](../wiki/images/tutorials/tutorial-form-designer.png)


Let's get started.

1. Start by creating a project called, `Tutorial Project`. Add any description and left the rest of the properties with their default values. Your screen should look like the following:

  ![Tutorial Project](../wiki/images/tutorials/tutorial-project.png)

2. Once you click save, you will go to the Project Dashboard. We will go straight to the screens.

  ![Tutorial Project Dashboard](../wiki/images/tutorials/tutorial-project-dashboard.png)

3. Click on the plus button to add a new screen.

  ![Tutorial Screen Properties](../wiki/images/tutorials/tutorial-form-screen-properties.png)

4. Now we are ready to start building our layout. There are a total of five elements that we will use. We will create each individually using an animation that you can follow along.

  ![Tutorial Form Animation](../wiki/images/tutorials/tutorial-form-screen.gif)

  Here is a recap of each of the elements that were added and settings. In each element we set specific classes and styles. The following is a breakdown for each element:

  Element | Host | Class | Content
  --- | --- | --- |---
  FORM |  | full-height padding-15 | 
  FORM-GROUP | FORM | form-group | 
  LABEL | FORM-GROUP | margin-right-10 | Enter your name
  INPUT | FORM-GROUP |  | 
  BUTTON | FORM | btn btn-primary | Say Hello

  ## Bindings
  The following are the bindings on the elements:

  Element | Attribute | Mode | Action
  --- | --- | --- |---
  INPUT | value | bind | currentItem.name

  ## Events
  The following are the events on the elements:

  Element | Attribute | Mode | Action
  --- | --- | --- |---
  BUTTON | click | delegate | actions.sayHello()

5. Save you work.

6. Click the Actions tab and enter the following code:

  ```javascript
  function (that, V) {

    function sayHello(e) {
      alert(`Hello ${that.currentItem.name}!`);
    }

   return {
      sayHello: sayHello
    };
  }
  ```

  **Note** We use `that` as a reference to the parent view model.

7. Save your work.

8. Click the Data tab and enter the following JSON:

  ```json
  {
    "currentItem": {
      "name": ""
    }
  }
  ```

9. Save your work.

10. Click on the Preview button and you should see something like the following:

  ![Tutorial Flexbox Preview](../wiki/images/tutorials/tutorial-form-preview.png)

That it! You have created your first form with bindings! Congratulations!

[ Tutorials ](tutorials/tutorials)

