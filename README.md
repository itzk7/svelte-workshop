## What we've done so far
We bootstrapped the app using npm create svelte@latest.

So far, we have added two routes: ```/expenses``` and ```/reports```. The ```/expenses``` route will render the ```ExpenseForm```, which is located at ```src/components/ExpenseForm.svelte```. The ExpenseForm includes category and date fields and is built using createForm from ```svelte-forms-lib```. The form data is stored in the Expense Store, which is located at ```src/stores/expenses.js```.


## Open terminal and run
```bash
npm i
npm run dev -- --open
```
You should be able to see,
![Alt text](image.png)

## Activity
Let's add an amount field input and implement validation so that the input value must fall within the range of 1 to 999,999. Ensure that the input value is printed to the console.
