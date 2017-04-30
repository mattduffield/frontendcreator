#Tutorial - Container with collapsible Panes, Part 2

In this part, we are going to create a Bootstrap Panel. These panels will be used in the third and final part of this series. Here is a screen shot of the layout we are going to build:

![Tutorial Project](../assets/images/tutorials/tutorial-panel.png)


Let's get started.

1. Start by creating a project called, `Tutorial Project`. Add any description and left the rest of the properties with their default values. Your screen should look like the following:

  ![Tutorial Project](../assets/images/tutorials/tutorial-project.png)

2. Once you click save, you will go to the Project Dashboard. We will go straight to the screens.

  ![Tutorial Project Dashboard](../assets/images/tutorials/tutorial-project-dashboard.png)

3. Click on the plus button to add a new screen.

  ![Tutorial Panel Properties](../assets/images/tutorials/tutorial-panel-properties.png)

4. Now we are ready to start building our layout. Click on the HTML tab and replace the following snippet in the editor. 

  ```html
  <div class="panel panel-black flex-column-1 overflow-auto">
    <div class="panel-heading">panel heading</div>
    <div class="panel-body">
      panel body here...
    </div>
  </div>
  ```

  This one is pretty straight forward. Here is a recap of each of the elements that were added and settings. In each element we set specific classes and styles. The following is a breakdown for each element:

  Element | Host | Class 
  --- | --- | --- |---
  DIV |  | panel panel-black flex-column-1 overflow-auto
  DIV | DIV | panel-heading
  DIV | DIV | panel-body

  Element | Host | Content
  --- | --- | ---
  DIV | DIV | panel heading
  DIV | DIV | panel body here...


5. Save you work.

6. Click on the Preview button and you should see something like the following:

  ![Tutorial Container Preview](../assets/images/tutorials/tutorial-panel-preview.gif)

That it! You have completed part 2! Congratulations!

[ Tutorials ](tutorials/tutorials) | [ Next -> ](container-part-3)
