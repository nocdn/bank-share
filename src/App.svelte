<script>
    import "./app.css";
    import Detail from "./Detail.svelte";
</script>

<main>
    <info-container>
        <svg
            width="26"
            height="26"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
        >
            <path
                d="M11 10.9794C11 10.4271 11.4477 9.97937 12 9.97937C12.5523 9.97937 13 10.4271 13 10.9794V16.9794C13 17.5317 12.5523 17.9794 12 17.9794C11.4477 17.9794 11 17.5317 11 16.9794V10.9794Z"
                fill="currentColor"
            />
            <path
                d="M12 6.05115C11.4477 6.05115 11 6.49886 11 7.05115C11 7.60343 11.4477 8.05115 12 8.05115C12.5523 8.05115 13 7.60343 13 7.05115C13 6.49886 12.5523 6.05115 12 6.05115Z"
                fill="currentColor"
            />
            <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2ZM4 12C4 16.4183 7.58172 20 12 20C16.4183 20 20 16.4183 20 12C20 7.58172 16.4183 4 12 4C7.58172 4 4 7.58172 4 12Z"
                fill="currentColor"
            />
        </svg>
        <p>Press on any piece of information to copy it to clipboard</p>
    </info-container>
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

<style lang="scss">
    main {
        padding: 3rem;

        display: flex;
        flex-direction: column;
        // center vertically
        align-items: center;
        gap: 1.5rem;

        width: 100vw;
        height: 100dvh;
    }

    info-container {
        display: grid;
        grid-template-columns: 1fr 5fr;
        align-items: center;
        gap: 0.75rem;
        margin-bottom: 1.5rem;

        opacity: 0.7;
        font-weight: 500;
        padding: 0 1rem;
    }

    info-container p {
        /* width: 45%; */
    }
</style>
