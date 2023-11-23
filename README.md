# Expense Tracker

## Developing

Install pkgs, and start the server and open the app in a new browser tab:

```bash
npm install
npm run dev -- --open
```

## Activity
Let's add functionality to delete expense 

Changes:
1. Create event named ```delete_expense```, dispatch expenseID on clicking delete icon
2. Add delete handler in ```src/routes/[...expense]/+page.svelte``` and set the handler for delete_expense event
