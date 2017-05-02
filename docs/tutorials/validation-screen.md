#Validation Screen Tutorial

The following are the steps required to use **FrontEnd Creator** to create a simple form with validation. Here is a screen shot of the layout we are going to build:

![Tutorial Project](../assets/images/tutorials/tutorial-validation-designer.png)

Let's get started.

1) Start by clicking on *Manage Projects* from navigation menu on the left pane.

![Tutorial Project](../assets/images/tutorials/tutorial-manage-projects.png)

2) Next, click on the New button and name the project, `Tutorial Project`. Add any description and leave the rest of the properties with their default values. You can add any tags you like to the project. Your should have something that looks like the following:

![Tutorial Project](../assets/images/tutorials/tutorial-project.png)

3) Once you click save, will notice that the project will automatically be added to the Manage Projects table as well as the navigation menu on the left:

![Tutorial Project Added](../assets/images/tutorials/tutorial-project-added.png)

4) Next, click on the Tutorial Project menu item from the navigation menu and select New Screen:

![Tutorial Project New Screen](../assets/images/tutorials/tutorial-project-new-screen.png)

5) Name the screen, `navigation-screen`. Add any description and pick any icon you wish for the screen. You can add any tags you like to the screen. You should have something that looks like the following:

![Tutorial Screen Properties](../assets/images/tutorials/tutorial-validation-screen-properties.png)

6) Clicking save will navigate you to the designer.

7) We are now ready to start building our layout. There are a total of eight elements that we will use. We will create each individually using a video that you can follow along.

{% youtube %}
  https://www.youtube.com/watch?v=VKfqn33OuLI
{% endyoutube %}
  
Here is a recap of each of the elements that were added and settings. In each element we set specific classes and styles. The following is a breakdown for each element:

Element | Host | Class | Content
------- | ---- | ----- | -------
FORM |  | padding-15 | 
FORM-GROUP | FORM | form-group | 
LABEL | FORM-GROUP |  | Email
INPUT | FORM-GROUP | form-control | 
FORM-GROUP | FORM | form-group | 
LABEL | FORM-GROUP |  | Age
INPUT | FORM-GROUP | form-control | 
BUTTON | FORM | btn btn-primary | Submit

## Attributes
The following are the bindings on the elements:

Element | Name | Value
---- | ---- | ---- | ----
FORM | validator | data-context.bind: currentItem; schema.bind: schema; 
FORM | data-context | dataContext

## Bindings
The following are the bindings on the elements:

Element | Attribute | Mode | Action
---- | ---- | ---- | ----
INPUT | value | bind | currentItem.email
INPUT | value | bind | currentItem.age

## Events
The following are the events on the elements:

Element | Attribute | Mode | Action
---- | ---- | ---- | ----
BUTTON | click | delegate | actions.submit()

8) Save you work.

9) Click the Actions tab and enter the following code:

```javascript
function (that, V) {

  function submit() {
    console.log(JSON.stringify(that.currentItem));
    if (that.validateFormFunc) {
      let isFormValid = that.validateFormFunc();
      if (!isFormValid) {
        that.notifier.growl({type: 'warn', message: `Please correct validation errors!`});
        return;
      }
      that.notifier.growl({type: 'success', message: `Form is valid!`});    
    }
  }
  
 return {
    submit: submit
  };
}
```

  **Note** We use `that` as a reference to the parent view model.

10) Save your work.

11) Click the Data tab and enter the following JSON:

```json
{
  "currentItem": {
    "email": "",
    "age": ""
  }
}
```

12) Save your work.

13) Click on the Schema tab and enter the following JSON:

```javascript
{
  "email": V.all([V.required(), V.email(null, "Not a valid email.")]),
  "age": V.all([V.required(), V.isNumeric(null, "Not a valid number.")])
}
```

14) Save your work.

15) Click on the Preview tab or the Preview button and you should see something like the video above.

That it! You have created your first validation form! Congratulations!
