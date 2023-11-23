<script>
    import Delete from "$lib/icons/delete-icon.svelte"
    export let category;
    export let expenseDate;
    export let amount = 0;
    export let expenseID;
</script>


<div class='card-content'>
    <p>
        {category}
    </p>
    <p>
        {expenseDate}
    </p>
    <p>
        {amount}
    </p>
    <button>
        <Delete />
    </button>    
</div>


<style>
    .card-content button {
        border: none;
        background: none;
        cursor: pointer;
    }
    .card-content {
        font-size: 18px;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-evenly;
        background: white;
    }

    .card-content p {
        width: 25%;
    }

    .card-content:first-child {
        border-bottom: 0.5px solid var(--grey-dark);
        background: #1414a6d1;
    }

    .card-content:first-child button{
        visibility: hidden;
        cursor: not-allowed;
    }

    .card-content:first-child p{
        color: white;
    }
</style>