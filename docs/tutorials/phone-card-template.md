# Phone Card Template
Being able to build reusable components is invaluable for developers and designers and **FrontEnd Creator** templates are no different. Consider the following phone card template:

![Phone Card Template](../images/entity-builder-quick-start.png)

This tutorial will walk you through the steps required to create the example from above using the **Template Builder**:


1. Navigate to the **Template Builder**
2. Create a new template by clicking on the New button
3. Name the template: `phone-card`
4. Select `Layout (Multiple Records)` for the Template Type
5. Enter the number `10` for the Order
6. Enter the number `1` for the Number of Records
7. Add the following HTML for the Template:
  ```html
  <div>
    <style>
      section.fec-phone-cards {
        min-height: 475px;
      }
      .fec-phone-card {
        position: relative;
        list-style: none;
        max-height: 450px;
        max-width: 300px;
        background-color: #424242;
        color: white;
        margin-bottom: 15px;
        display: grid;
        grid-gap: 0;
        grid-template-rows: 1fr 6fr 1fr 1fr;
        box-shadow: 5px 5px 5px lightgray;
      }
      .fec-phone-card .image > img {
        flex-shrink: 0;
        min-width: 100%;
        min-height: 100%;
        border-radius: 150px;
      }
      .fec-phone-card .buttons > button {
        margin: 10px;
        width: 100px;
        height: 40px;
        font-size: large;
      }
      .fec-phone-card .green {
        background-color: green;
        color: white;
      }
      .fec-phone-card .red {
        background-color: red;
        color: white;
      }
      .fec-phone-card:hover [title]:before {
        position:absolute;
        float: left;
        color: rgba(128,200,255,1.0); 
        background-color: rgba(0,0,0,0.5); 
        content: attr(title);
        padding: 4px;
        border-radius: 10px;
      }
    </style>  
    <section class="fec-phone-cards">
      <li class="fec-phone-card" repeat.for="item of data" with.bind="item">
        <div class="margin-left-right-20">
          <h3 class="flex-row-1 justify-content-center">Incoming call...</h3>
        </div>
        <div title="$0" class="image padding-20 flex-row-1 justify-content-center">
          [0]
        </div>
        <div class="product margin-left-right-20">
          <h3 class="flex-row-1 justify-content-center">John Doe</h3>
        </div>
        <div class="buttons margin-left-right-20 margin-bottom-10 flex-row-1 justify-content-center">
          <button class="green flat">Accept</button>
          <button class="red flat">Decline</button>
        </div>
      </li>
    </section>
  </div>
  ```
8. Switch over to the Sample Entity tab and enter in the following:
  ```json
  {
    "name": "phone-card",
    "fields": [
      {
        "name": "poster",
        "alt": "",
        "type": "string",
        "defaultElement": "imgLarge",
        "includeField": true,
        "isRequired": false,
        "index": 0
      }
    ]
  }
  ```
9. Next, click on the Refresh button to render the template
10. You can change the Number of Records to see more of these templates and then click the Reload button followed by the Render button re-render the template
11. Trying changing out some of the embedded styles and click the Refresh button to see them applied 

That should do it! You should now have a template that looks something like the following with the exception of the image as it is random:

![Phone Card Template](../images/entity-builder-quick-start.png)

Notice, that we included some CSS to take advantage of the `title` attribute in the template. This allows to indicate *placeholders* that are substituted during the render phase from the sample entity. The following is the same screen but with the mouse hovering over the template:

![Phone Card Template](../images/entity-builder-quick-start-hover.png)

As you can see, we see that there is a single *placeholder*. You can have as many placeholders as you like in a template. Just be sure that the corresponding entity has as many fields. Also remember that the index propertty of the fields is how the fields are ordered for matching the *placeholder* values.

Hopefully, you see how easy it is to create templates and visualize them. In the future, we will have the **Template Builder** available to the designer surface so that you can quickly create really nice looking screen layouts!
