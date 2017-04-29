# Template Builder

The template builder allows you to quickly create templates that work off of entities. To allow for the most flexibility, you must provide a sample entity. The easiest way to do this is create an entity first in the **Entity Builder** and then copy the JSON and simply paste it in the Sample Entity tab.

![Template Builder](images/template-builder.gif)

As you can see from the animation above, it is very easy to make quick changes to your template and re-render them so that you can see what it looks like immediately. In the animation above, we are simply changing out some of the style settings but you could change out the HTML as well and test that.

The Template tab allows you to create templates quickly and render them on the right side. You have the option to use placeholders for where string interpolation will occur or simply provide your own. 

Most of the templates created by **FrontEnd Creator** embed styles into the template so that you can visualize them immediately. However, it is recommended that you pull those styles and put them in a Styles editor and reference them in the corresponding screen which will host the template.

The template builder has the following properties:

* ID - this is readonly and represents the template ID
* Name - this is the name of the template
* Description - this is the description of the template
* Template Type - this determines what type of template you are building. You have the following options:
  * Form Edit - this type represents an editable form for use with a single record. It will only show the Sample Entity tab
  * Form View - this type represents a view only form for use with a single record. It will only show the Sample Entity tab
  * Table Edit - this type represents an editable table for use with multiple records. It will only show the Sample Entity tab
  * Table View - this type represents a view only table for use with multiple records. It will only show the Sample Entity tab
  * Layout (Single Record) - this type allows you to provide a template for use with a single record using the Template tab
  * Layout (Multiple Records) - this type allows you to privide a template that will repeat across multiple records using the Template tab
* Order - this represents the order in which you would want the templates displayed for selection
* Number of Records - this indicates the number of records to be generated while previewing the template. It default value is one (1)

After the properties section, you have the Preview section. It contains two buttons and the preview area. The following is a description of each button:
* Refresh - this button will re-render the template and apply any data if any placeholders have been used. The mnemonic to execute this button is `Ctrl|Cmd + R`
* Reload - this button will re-load data based on the `Number of Records` propertry. You still need to click the Refresh button to re-render the template with the new data. The mnemonic to execute this button is `Ctrl|Cmd + D`

The template builder introduces a new concept called, **Placeholders**. This is how the template builder can remain generic and yet work with an existing entity to provide bindings on your templates when rendered. The following is an example of a template with several *placeholders*:

```html
<ul class="product-card grid">
  <li class="card" repeat.for="item of data" with.bind="item">
    <header title="$0">[0]</header>
    <main title="$1">[1]</main>
  </li>
</ul>

```

This template has two placeholders for real data to be represented. We have a position in the *header* element as well as in the *main* element. Observe that we use the brackets `[<number>]` with an index position inside to identify the order of the values rendered.

The template works in conjunction with an Entity. This is the reason for the Sample Entity tab. The following is the corresponding entity definition used with this template:

```json
{
  "name": "product",
  "fields": [
    {
      "name": "name",
      "alt": "",
      "type": "string",
      "defaultElement": "name",
      "includeField": true,
      "isRequired": false,
      "index": 0
    },
    {
      "name": "description",
      "alt": "",
      "type": "string",
      "defaultElement": "text",
      "includeField": true,
      "isRequired": false,
      "index": 1
    }
  ]
}
```

The important thing to note here is that we have two field entries. Each field has an `index` property. This should correspond to the *placeholder* you defined in template. So for the template markup we just saw, we are putting a string that represents a person name in the first (0) index position and a text string in second (1) index position.

To understand what your options are a given field, please refer to the documentation on [ Entity Builder ](entity-builder) and look at the corresponding tables.


[ <- Previous ](application-export) | [ Home ](home) | [ Next -> ](translation-builder)
