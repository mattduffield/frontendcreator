# Event Handling

The next animation shows adding a click event to a button:

![Designer data-bind](../../../assets/images/click-delegate.gif)

After we have setup the click event, we can verify that it is working against a function in our Actions tab as well as see it live in the Preview tab or launching a new Preview browser tab.

**Remember** You must save to get the changes to be reflected in the Preview.

![Designer data-bind](../../../assets/images/click-delegate-preview.gif)

### Steps

In the previous animations, you saw how we wired up the click event on the button element using the following command:

`click.delegate="actions.sample()"`

We next need to ensure that we have an function named, "sample", in the Actions tab.

We can see that we exactly this when we look at the Actions tab here:

![Designer Data tab](../../../assets/images/designer-actions.png)

### Events

The Events section is used to define all of your event handlers for a given element. It consists of three parts:

* **Attribute** - this is the attribute for which the event handler is associated with, e.g. 'click', 'keydown', 'change', etc.
* **Mode** - this is how the event is raised, e.g. 'delegate', 'trigger', or 'call'
* **Action** - this is the function reference that will be called when the event is raised

You have the ability to add or remove as many events as you like. You must click on the blue check button to apply your changes to the element. 

The following is a screen shot of the events section:

![Designer Property Grid Events](../../../assets/images/designer-property-grid-events.png)
