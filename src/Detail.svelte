<script>
    export let name;
    export let sortCode;
    export let accountNumber;

    export let color;

    // Variables to control the temporary icon display
    let isSortCodeCopied = false;
    let isAccountNumberCopied = false;

    // On click of the account number or sort code, copy the value to the clipboard and show SVG for 0.75 seconds
    function copyToClipboard(value, type) {
        navigator.clipboard.writeText(value);

        // Set the appropriate variable to true to show the SVG icon
        if (type === "sortCode") {
            isSortCodeCopied = true;
        } else if (type === "accountNumber") {
            isAccountNumberCopied = true;
        }

        // After 0.75 seconds, revert back to the original value
        setTimeout(() => {
            if (type === "sortCode") {
                isSortCodeCopied = false;
            } else if (type === "accountNumber") {
                isAccountNumberCopied = false;
            }
        }, 750);
    }
</script>

<detail-container class={color}>
    <h2>{name}</h2>
    <div class="numbers-container">
        <a
            href={null}
            on:click={() => copyToClipboard(sortCode, "sortCode")}
            class="account-sort-code mono"
        >
            {#if isSortCodeCopied}
                <svg
                    width="18"
                    height="18"
                    viewBox="0 0 24 24"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M10.2426 16.3137L6 12.071L7.41421 10.6568L10.2426 13.4853L15.8995 7.8284L17.3137 9.24262L10.2426 16.3137Z"
                        fill="currentColor"
                    />
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M1 12C1 5.92487 5.92487 1 12 1C18.0751 1 23 5.92487 23 12C23 18.0751 18.0751 23 12 23C5.92487 23 1 18.0751 1 12ZM12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3C16.9706 3 21 7.02944 21 12C21 16.9706 16.9706 21 12 21Z"
                        fill="currentColor"
                    />
                </svg>
            {:else}
                {sortCode}
            {/if}
        </a>
        <a
            href={null}
            on:click={() => copyToClipboard(accountNumber, "accountNumber")}
            class="account-number mono"
        >
            {#if isAccountNumberCopied}
                <svg
                    width="18"
                    height="18"
                    viewBox="0 0 24 24"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M10.2426 16.3137L6 12.071L7.41421 10.6568L10.2426 13.4853L15.8995 7.8284L17.3137 9.24262L10.2426 16.3137Z"
                        fill="currentColor"
                    />
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M1 12C1 5.92487 5.92487 1 12 1C18.0751 1 23 5.92487 23 12C23 18.0751 18.0751 23 12 23C5.92487 23 1 18.0751 1 12ZM12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3C16.9706 3 21 7.02944 21 12C21 16.9706 16.9706 21 12 21Z"
                        fill="currentColor"
                    />
                </svg>
            {:else}
                {accountNumber}
            {/if}
        </a>
    </div>
</detail-container>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap");

    detail-container {
        width: 16rem;
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
        background-color: #f3f4f6;
        color: #212936;
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

    a {
        outline: 2px dotted #000;
        border-radius: 6px;
        padding: 0.4rem;
        width: 6.5rem;
        height: 2rem;
        display: grid;
        place-content: center;
        cursor: pointer;
    }

    .numbers-container {
        display: flex;
        gap: 1.5rem;
    }

    .green {
        background-color: #ecf7ed;
        color: #143d19;
    }

    .orange {
        background-color: #fff3e0;
        color: #872f10;
    }

    .red {
        background-color: #feeae9;
        color: #861717;
    }

    .pink {
        background-color: #fdeef7;
        color: #a81650;
    }

    .blue {
        background-color: #e5f4fb;
        color: #142f39;
    }

    .purple {
        background-color: #e7ebfa;
        color: #15183e;
    }
</style>
