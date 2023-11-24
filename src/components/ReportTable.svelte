<script>
    import { expenses } from "../stores/expenses.js";
    import Chart from 'chart.js/auto';
    import { onMount } from 'svelte';

    console.log('From report component', $expenses)

    // TODO: use $expenses to generate categories as label and its total amount as sum
    const labels = ["abc", "def", "ghi"]
    const values = [10, 20, 40]
    const totalExpense = 9999

    let report;
    const data = {
        labels: labels,
        datasets: [
            {
                label: 'My Expense',
                data: values,
                hoverOffset: 4,
                borderWidth: 0
            }
        ]
    };
    const config = {
        type: 'pie',
        data: data,
        options: {
            responsive: true,
            spacing: 2,
            width: 300,
            height: 200,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom',
                    display: true,
                    labels: {
                        usePointStyle: true,
                        padding: 20,
                        font: {
                            size: 18
                        }
                    }
                },
                title: {
                    display: true,
                    text: `My total expense: ₹ ${totalExpense}`,
                    font: {
                        size: 20
                    }
                }
            }
        }
    };
    onMount(()=> {
        if (report) {
            const ctx = report.getContext('2d');
            // // Initialize chart using config set
            var myChart = new Chart(ctx, config);
        }
    })
	</script>

<div class="report-container">
    {#if totalExpense}
    <canvas bind:this={report}></canvas>
    {:else}
    <h3>Nothing here, Add expense to view report</h3>
    {/if}
</div>

<style>
    .report-container{ 
        display: flex;
        justify-content: center;
        align-items: center;
        height: 70vh;
    }

</style>