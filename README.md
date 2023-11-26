To run the app
```bash
npm run dev -- --open
```
Now you should be able to see, the list of expenses


## Activity
Let's add functionality to delete expense 

TODO:
1. Create event named ```delete_expense```, dispatch expenseID on clicking delete icon
2. Add delete handler to delete expense in ```src/routes/[...expense]/+page.svelte``` and set the handler for delete_expense event

## Reference
Basics session link: https://svelte.dev/repl/b42abb120dcc482e8c34fbcb14a5cad8?version=4.2.7
