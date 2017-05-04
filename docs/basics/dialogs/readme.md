# Dialogs

**FrontEnd Creator** uses the aurelia-dialog plugin to provide dialogs. It has been wrapped to allow for an easy workflow. 

Dialogs are treated just like regular screens but have slightly different behavior. Instead of responding to routes and being displayed, they respond to user interactions. You have the ability to craft the dialog as much as you like within the guidelines of the aurelia-dialog plugin.

The following screenshot is an example of a `screen-dialog` that is used when creating a new or editing an existing screen:

![Dialogs](../../assets/images/confirm-dialog-new.png)

Dialog screens are stored just like regular screens. We use a `dataService` reference to make a fetch call to grab a dialog by its Id. We next use a `dialogService` that handles rendering the dialog to the screen. The function, `show2`, takes a single argument. The following is a signagure of the `payload` parameter:

Property | Description
-------- | -----------
screen | this identifies which dialog screen to use. You must have already loaded the screen using the `dataService`
owner | this identifies under what context the dialog is rendered
data | this represents a data object that your dialog can bind to

The function `show2` is promise-based and will return a promise if dialog screen called, `controller.ok(...)` passing whatever value they wish. You will be able to interrogate the `response` object and make your decision as how you want to proceed.

Refer to the [ Dialog Tutorial ](../../tutorials/dialog.md) for tutorial on working with dialogs in your screens.


> #### primary::
> Please refer to the [ Aurelia Dialog](https://github.com/aurelia/dialog) documentation to learn more about using dialogs.
