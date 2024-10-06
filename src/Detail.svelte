<script>
    export let name;
    export let sortCode;
    export let accountNumber;
</script>

<detail-container>
    <h2>{name}</h2>
    <p class="account-sort-code mono">{sortCode}</p>
    <p class="account-number mono">{accountNumber}</p>
</detail-container>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap");

    detail-container {
        width: 16rem;
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
        background-color: #f2e6eb;
        padding: 1rem;
        border-radius: 0.875rem;
    }

    h2 {
        font-family: "Inter", sans-serif;
        font-size: 1.5rem;
        font-weight: 600;
        line-height: 1.25;
        margin: 0;
    }

    .mono {
        font-family: "SF Mono", monospace;
    }
</style>
