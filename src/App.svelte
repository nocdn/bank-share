<script>
    import "./app.css";
    import Detail from "./Detail.svelte";
    import { Button } from "$lib/components/ui/button";
    import { Toaster } from "$lib/components/ui/sonner";
</script>

<main>
    <Detail name="John Doe" sortCode="12-34-56" accountNumber="78008093"
    ></Detail>
    <Detail name="Bartosz Bak" sortCode="98-19-77" accountNumber="98562028"
    ></Detail>
    <Button on:click={() => toast("Hello world")}>Show toast</Button>
</main>

<style>
    main {
        padding: 3rem;

        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }
</style>
