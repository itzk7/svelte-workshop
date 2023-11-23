<script>
    import ExpenseRow from "./ExpenseRow.svelte";
    export let expenses = []
    const expenseHeader = {}
    expenseHeader['expenseID']='ID'
    expenseHeader['category']='Category'
    expenseHeader['amount']='Amount(₹)'
    expenseHeader['expenseDate']='Expense Date'
</script>

{#if expenses.length > 0}
    <h3>Expenses</h3>
    <div class="card-container">
        <ExpenseRow {...expenseHeader}/>
        <!-- TODO: Iterate each expenses and call ExpenseRow component here -->
    </div>
{/if}


<style>
     .card-container {
        width: 70%;
        background: var(--primary-light) ;
        border-radius: 5px;
        border: 1px solid var(--grey-dark);
        margin-bottom: 10px;
    }

    @media (max-width: 900px) {
    .card-container {
        width: 90%;
    }

}
</style>