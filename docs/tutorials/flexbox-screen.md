#Flexbox Screen Tutorial

Layout has always been a challenge when it comes to writing web applications forcing you to write an enormous amount of CSS or rely on a third-party library. Flexbox is one of the new kids on the block that has made this type of work easier, with minimal CSS. In this tutorial, we will be building the following layout, sometimes known as the holy grail in layout.

![Tutorial Flexbox](../assets/images/tutorials/tutorial-flexbox.png)

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

![Tutorial Screen Properties](../assets/images/tutorials/tutorial-flexbox-screen-properties.png)

6) Clicking save will navigate you to the designer.


7) Now we are ready to start building our layout. There are a total of seven elements that we will use. We will create each individually using an animation that you can follow along.

![Tutorial Flexbox Animation](../assets/images/tutorials/tutorial-flexbox-screen.gif)

Here is a recap of each of the elements that were added and settings. In each element we set specific classes and styles. The following is a breakdown for each element:

Element | Host | Class | Style
--- | --- | --- |---
DIV |  | flex-column full-height | 
HEADER | DIV | flex-row-none | background-color: lightblue;
MAIN | DIV | flex-row-1 | 
SIDEBAR | MAIN | flex-row-1 justify-content-center | background-color: orange;
ARTICLE | MAIN | flex-row-3 align-items-center justify-content-center | background-color: cornsilk;
ASIDE | MAIN | flex-row-1 | background-color: mistyrose;
FOOTER | DIV | flex-row-none justify-content-end | background-color: lightgreen;

8) Save you work.

9) Click on the Preview button and you should see your layout like the following:

![Tutorial Flexbox Preview](../assets/images/tutorials/tutorial-flexbox-preview.png)

That it! You have created your first Flexbox layout! Congratulations!
