## To run the app
```bash
npm run dev -- --open
```
Now the delete option will be working fine, and in the reports tab you can see the chart with the dummy values. The chart is generated using https://www.chartjs.org/docs/latest/charts/doughnut.html#pie. 

#### Now how this chart works in ```src/components/ReportTable.svelte```

The chart requires a canvas context, which we obtain by binding the component property report using ```bind:this={report}```. We use this context to create the chart in the ```onMount``` lifecycle method

## Activity
Let's calculate the total amount, the categories and their totals, and fix the values and labels in the chart.

### TODO:
In ```src/components/ReportTable.svelte``` Calculate correct totalExpenses, categories and its aggregated amount using $expenses

set the categories in labels and set its total amount in values

Let's say you have 4 expenses: ```[{'rent': 4000}, {'gadgets': 100}, {'food': 500}, {'rent': 3000}]```.

Then the labels and values should be ```['rent', 'gadgets', 'food'] and [7000, 100, 500]```, respectively
