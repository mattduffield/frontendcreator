#REST API Screen Tutorial

This tutorial will walk you through creating a script that makes use of the HTTP fetch client and gets random user data from a REST API. Here is a screen shot of the layout we are going to build:

![Tutorial Project](images/tutorials/tutorial-randomuser-designer.png)

Let's get started.

1. Start by creating a project called, `Tutorial Project`. Add any description and left the rest of the properties with their default values. Your screen should look like the following:

  ![Tutorial Project](images/tutorials/tutorial-project.png)

2. Once you click save, you will go to the Project Dashboard. We will start with the script first.

  ![Tutorial Project Dashboard](images/tutorials/tutorial-project-dashboard.png)

3. Click on the Scripts button to lauch the Project Scripts editor. Here we will add our first script. Enter the following into the Script Properties pane:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-randomuser-script.png)

4. Next, type in the following code into the editor:
  ```javascript
  @inject(HttpFetchClient)
  class RandomUser {
    constructor(http) {
      this.http = http;
      this.baseUrl = `https://randomuser.me/`;
      this.http.configure(config => {
        config
          .withBaseUrl(this.baseUrl)
          .withDefaults({
            headers: {
              'Accept': 'application/json',
              'X-Requested-With': 'Fetch'
            }
          });
      });
    }

    getUsers(numberUsers = 10) {
      let path = `api?results=${numberUsers}`;
      return this.http.fetch(path)
        .then(response => response.json());
    }
  }
  ```

5. As you can see we are using a standard ES6 class. We are injecting the HttpFetchClient into our constructor. Inside the constructor, we are configuring our fetch client. Finally, we have a single method: `getUsers`. It takes a single parameter to tell us how many users to return from our call.

6. Click the save button and the script should now show up on the left dock-pane.

7. We can now click the Back button and then select the Screens button. Click on the plus button to add a new screen.

  ![Tutorial Project Dashboard](images/tutorials/tutorial-randomusers-properties.png)

8. Click save and you will now be navigated to the designer. Select the Scripts tab and then click on the plus button to add the RandomUser script to the bottom of the designer as show below:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-randomusers-add-script.png)

9. Now, click on the HTML tab and copy and paste the following code into the editor:

  ```html
  <div class="users drag-container drag-item">
    <style>
      .users {
        display: flex;
        flex-flow: column wrap;
        justify-content: center;
        align-items: center;
        height: 100%;
        background-color: lightgray;
      }
      .users .user {
        display: flex;
        flex-flow: column;
        flex: none;      
        align-items: center;
        background-color: white;
        border-radius: 5px;
        height: 200px;
        width: 185px;
        padding: 10px;
        margin: 15px;
      }
      .users .user img {
        flex: none;
        height: 150px;
        width: 150px;
      }
      .users .user span {
        flex: none;
        font-size: large;
      }
    </style>
    <div class="user drag-container drag-item" repeat.for="user of users">
      <img class="drag-item" src.bind="user.picture.medium">
      <span class="flex-1">${user.name.first} ${user.name.last}</span>
    </div>
  </div>
  ```

10. Save you work.

11. Click the Actions tab and copy and paste the following code into the editor:
  ```javascript
  function (that, V) {
    function attached() {
      that.randomUser = that.classBuilder(that.Script.RandomUser,
        that.Script.RandomUser_inject);
      return that.randomUser.getUsers(15)
        .then(data => that.users = data.results);
    }
    
    return {
      attached: attached
    };
  }
  ```
  **Note** We use `that` as a reference to the parent view model.
  **Script** Take note that all scripts are referenced from the `Script` object.

  We are using a helper function that is exposed by our hosting view-model, `classBuilder`. It is this function that does the actual creation and injection of our dependencies and returns us back an instance. As you can see, the `classBuilder` function expects two arguments: RandomUser and RandomUser_inject. **FrontEnd Creator** creates the second object for us when the screen is first initialized and a script has been included.

  Next, we simply call the getUsers and then assign our `users` object once the promise returns.

12. Save your work.

13. Click on the Preview button and you should see something like the following:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-randomusers-preview.png)

14. Congratulations! You have finished this tutorial!!

[ Tutorials ](tutorials/tutorials)

