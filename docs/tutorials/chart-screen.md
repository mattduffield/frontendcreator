#Chart Screen Tutorial

The following are the steps required to use **FrontEnd Creator** and build a chart. It will make use of the Scripts capability as well as load the ChartJS library on demand.

Let's get started.

1. Start by creating a project called, `Tutorial Project`. Add any description and left the rest of the properties with their default values. Your screen should look like the following:

  ![Tutorial Project](images/tutorials/tutorial-project.png)

2. Once you click save, you will go to the Project Dashboard. We will start with the script first.

  ![Tutorial Project Dashboard](images/tutorials/tutorial-project-dashboard.png)

3. Click on the Scripts button to lauch the Project Scripts editor. Here we will add our first script. Enter the following into the Script Properties pane:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-script-properties.png)

4. Next, type in the following code into the editor:
  ```javascript
  class ChartManager {

    constructor() {
      this.loadJS('https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.4.0/Chart.bundle.js', 
        this.chartCallback, document.body);      
    }
    
    loadJS(url, callback, target) {
      let scriptTag = document.createElement('script');
      scriptTag.src = url;
      scriptTag.onload = callback;
      target.appendChild(scriptTag);
    }    
    
    chartCallback(e) {
      let ctx = document.getElementById("myChart");
      let myChart = new Chart(ctx, {
        type: 'bar',
        data: {
          labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
          datasets: [{
            label: '# of Votes',
            data: [4, 1, 3, 5, 2, 3],
            backgroundColor: [
              'rgba(255, 99, 132, 0.2)',
              'rgba(54, 162, 235, 0.2)',
              'rgba(255, 206, 86, 0.2)',
              'rgba(75, 192, 192, 0.2)',
              'rgba(153, 102, 255, 0.2)',
              'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
              'rgba(255,99,132,1)',
              'rgba(54, 162, 235, 1)',
              'rgba(255, 206, 86, 1)',
              'rgba(75, 192, 192, 1)',
              'rgba(153, 102, 255, 1)',
              'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
          }]
        },
        options: {
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero:true
              }
            }]
          }
        }
      });
    }    
  }
  ```

5. As you can see we are using a standard ES6 class. We have a helper method `loadJS` that allows us to add any JavaScript library, preferable on a CDN. When the ChartJS library loads, we then call the `chartCallback` method which does all the heavy work of creating the Chart. Take note that we are referencing a ID tag `myChart`. We will add that when we create our screen.

6. Click the save button and the script should now show up on the left dock-pane.

7. We can now click the Back button and then select the Screens button. Click on the plus button to add a new screen.

  ![Tutorial Project Dashboard](images/tutorials/tutorial-screen-properties.png)

8. Click save and you will now be navigated to the designer. Select the Scripts tab and then click on the plus button to add the ChartManager script to the bottom of the designer as show below:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-designer-add-script.png)

9. Now, click on the Toolbox tab and type in the word, `canvas` to search for the Canvas. 
  - Drag the canvas onto the designer surface. 
  - Click on the Canvas to select it.
  - Under the Attributes section click the plus button and type in `id` for the name and `myChart` for the value.
  - Click the blue check button to apply the changes.

  ![Tutorial Project Dashboard](images/tutorials/tutorial-designer-add-canvas.png)

10. Save you work.

11. Click the Actions tab and enter the following code:
  ```javascript
  function (that, V) {

    function attached() {
      that.chartManager = new that.Script.ChartManager();
    }

   return {
      attached: attached
    };
  }
  ```
  **Note** We use `that` as a reference to the parent view model.
  **Script** Take note that all scripts are referenced from the `Script` object.

12. Save your work.

13. Click on the Preview button and you should see something like the following:

  ![Tutorial Project Dashboard](images/tutorials/tutorial-chart-preview.png)

14. Congratulations! You have finished this tutorial!!

[ Tutorials ](tutorials/tutorials)

