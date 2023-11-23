<script>
    import ExpenseForm from "../../components/ExpenseForm.svelte";
    import { expenses } from "../../stores/expenses.js";

function addExpense(e) {
    expenses.add(e.detail)
    console.log($expenses)
}

</script>

<div class="container">
    <ExpenseForm on:add_expense={addExpense} />
    <!-- TODO: Add ExpenseList component here and set $expenses as a property-->
</div>

<style>
    .container {
        display: flex;
        flex-flow: column;
        align-items: center;
    }
</style>