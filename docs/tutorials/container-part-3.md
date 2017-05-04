#Container Tutorial - Part 3 Composition

So far, we have built two separate components. We have a container with sliding panes and we now have a panel. In this tutorial, we are going to bring it all together by using composition and build out our container now with the panels included. Here is a screen shot of the layout we are going to build:

![Tutorial Project](../assets/images/tutorials/tutorial-container-panel.png)


Let's get started.

1) Start by clicking on *Manage Projects* from navigation menu on the left pane.

![Tutorial Project](../assets/images/tutorials/tutorial-manage-projects.png)

2) Next, click on the New button and name the project, `Tutorial Project`. Add any description and leave the rest of the properties with their default values. You can add any tags you like to the project. Your should have something that looks like the following:

![Tutorial Project](../assets/images/tutorials/tutorial-project.png)

3) Once you click save, will notice that the project will automatically be added to the Manage Projects table as well as the navigation menu on the left:

![Tutorial Project Added](../assets/images/tutorials/tutorial-project-added.png)

4) Next, click on the Tutorial Project menu item from the navigation menu and select New Screen:

![Tutorial Project New Screen](../assets/images/tutorials/tutorial-project-new-screen.png)

5) Name the screen, `container-panel`. Add any description and pick any icon you wish for the screen. You can add any tags you like to the screen. You should have something that looks like the following:

![Tutorial Panel Properties](../assets/images/tutorials/tutorial-container3-properties.png)

6) Now we are ready to start building our layout. The following video will walk you through the steps required to compose the screen:

{% youtube %}
  https://youtu.be/B6M1p2ZV0xE
{% endyoutube %}


We will simply be dragged the `container` and `panel` components onto the designer. We also adjusted some content as well as removed some `background-color` styles.

**Note:** Although, this is powerful and allows you to compose your screens together quickly, it lacks the ability to reference the `container` and `panel` as custom elements. In the next tutorial, we will look at an alternative route to building this out using custom elements.

8) Save you work.

9) Click on the Preview button and you should see something like the following:

![Tutorial Container Preview](../assets/images/tutorials/tutorial-container-panel-preview.gif)

That's it! You have completed part 3! Congratulations!
