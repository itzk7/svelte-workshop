# Expense Tracker

## To run the app
```bash
npm run dev -- --open
```

## Activity
Let's calculate the total amount, the categories and their totals, and fix the values and labels in the chart.

### TODO:
In ```src/components/ReportTable.svelte``` Calculate correct totalExpenses, categories and its aggregated amount using $expenses

set the categories in labels and set its total amount in values

Let's say you have 4 expenses: [{'rent': 4000}, {'gadgets': 100}, {'food': 500}, {'rent': 3000}].

Then the labels and values should be ['rent', 'gadgets', 'food'] and [7000, 100, 500], respectively

## Reference
Basics session link: https://svelte.dev/repl/b42abb120dcc482e8c34fbcb14a5cad8?version=4.2.7

Chartjs: https://www.chartjs.org/docs/latest/charts/doughnut.html#pie