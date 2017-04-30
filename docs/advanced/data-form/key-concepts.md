#DataForm

The data-form custom element allows you to generate data forms without writing a single line of code. It does this by creating an element for every key in a given data object. It also has the ability to validate data entry using a validator.

The following is an example of the HTML markup required to get a data-form configured. If you create a new screen and select Is DataForm, then this will already be set for you:

![DataFrom HTML](../../assets/images/data-form-html.png)

Here is a screen shot of the Schema tab:

![DataFrom Schema](../../assets/images/designer-schema.png)

You can learn more about using the Validator [ here ](../validation/key-concepts.md).

Here is a screen shot of the Data tab:

![DataFrom Data](../../assets/images/designer-data.png)

Here you can see the data-form in action:

![DataFrom](../../assets/images/data-form.gif)

As you can see from the animation, you can use the validation summary to navigate to each individual validation error.

The data-form has the following attributes:

* **auto-generate-fields** - You can set this to `true` and let the data-form generate the fields for you.
* **current-item** - You bind this attribute to your underlying data object.
* **validate-on-blur** - You can set this to `true` so that validation will occur on blur.
* **schema** - You bind this attribute to your underlying schema object.

**Remember** You can learn more about using [ Validation - Advanced Concepts ](../validation/key-concepts.md).
