<script>
    import "./app.css";
    import Detail from "./Detail.svelte";
</script>

<main>
    <Detail
        name="Bartosz Bak"
        sortCode="98-19-77"
        accountNumber="98562028"
        color="pink"
    ></Detail>
    <Detail
        name="Michael Scott"
        sortCode="12-34-56"
        accountNumber="78008093"
        color="orange"
    ></Detail>
    <Detail
        name="Pam Beasley"
        sortCode="12-34-56"
        accountNumber="78008093"
        color="red"
    ></Detail>
    <Detail
        name="Annie January"
        sortCode="12-34-56"
        accountNumber="78008093"
        color="blue"
    ></Detail>
    <Detail
        name="Jake Peralta"
        sortCode="98-19-77"
        accountNumber="98562028"
        color="purple"
    ></Detail>
    <Detail
        name="Jim Halpert"
        sortCode="12-34-56"
        accountNumber="78008093"
        color="green"
    ></Detail>
</main>

<style>
    main {
        padding: 3rem;

        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }
</style>
