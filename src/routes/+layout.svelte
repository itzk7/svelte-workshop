<script>
    import { page } from '$app/stores';
    console.log($page.url.pathname)
</script>
<div class="app-container">
    <nav class = "nav-container">
        <div class="nav-elements">
            <ul>
                <li>
                    <a href="/expense" class:active={$page.url.pathname == "/expense"}>
                        Expense
                    </a>
                </li>
                <li>
                    <a href="/reports" class:active={$page.url.pathname == "/reports"}>
                        Reports
                    </a>
                </li>
            </ul>
        </div>
    </nav>


    <slot/>

    <div class="footer">
        <!-- svelte-ignore a11y-distracting-elements -->
        <marquee><h2>Let's calculate the total amount, the categories and their totals, and fix the values and labels in the chart.
        </h2></marquee>
    </div>
</div>
<style>
:root {
    --primary-light: #1414a6d1;
    --primary: #1414a6d1;
    --primary-dark: #1414a6d1;
    --secondary: #1e2145;
    --white: #fff;
    --grey: #e6e6ff;
    --grey-dark: #6d7098;
    --red: #ff6b6b;
  }

  .nav-container {
    background-color: var(--primary);
    border-radius: 4px;
    position: relative;
  }

    .nav-elements ul {
        display: flex;
        list-style-type: none;
    }

    .nav-elements ul li:not(:last-child) {
        margin-right: 60px;
    }

    .nav-elements ul a {
        font-size: 18px;
        font-weight: 400;
        color: white;
        text-decoration: none;
    }

    .nav-elements ul a.active{
        color: white;
        font-weight: 500;
        position: relative;
    }

    .nav-elements ul li a.active::after {
        content: "";
        position: absolute;
        bottom: -4px;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: white;
    }

    .footer {
        margin-top: auto;
    }

    .app-container {
        display: flex;
        flex-direction: column;
        flex: 1;
        height: 98vh;
    }
</style>