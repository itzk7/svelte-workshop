# Expense Tracker

## Developing

Install pkgs, and start the server and open the app in a new browser tab:

```bash
npm install
npm run dev -- --open
```

## Activity
Let's show added expense in the list,

Changes:
1. Add ExpenseList componet in ```src/routes/[...expense]/+page.svelte```
2. Pass expenses properties to the ExpenseList component ```src/components/ExpenseList.svelte```
