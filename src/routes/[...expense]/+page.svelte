<script>
    import ExpenseForm from "../../components/ExpenseForm.svelte";
    import { expenses } from "../../stores/expenses.js";
    import ExpenseList from "../../components/ExpenseList.svelte";


    // TODO: Add deleteExpense similar to addExpense
    // and set it for delete_expense event

    function addExpense(e) {
        expenses.add(e.detail)
        console.log($expenses)
    }

</script>

<div class="container">
    <ExpenseForm on:add_expense={addExpense} />
    <ExpenseList expenses={$expenses} />
</div>

<style>
    .container {
        display: flex;
        flex-flow: column;
        align-items: center;
    }
</style>