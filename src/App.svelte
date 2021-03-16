<script>
    import { onMount } from "svelte";

    import Tailwind from "./Tailwind.svelte";
    import { ethStore, web3, selectedAccount, connected } from "svelte-web3";

    // import getWeb3 from "./utils/getWeb3.js";

    onMount(async () => {
        ethStore.setBrowserProvider();
        console.log($selectedAccount);
    });
</script>

<Tailwind />

<div class="flex flex-col items-center justify-center w-screen h-screen">
    <h1 class="mb-5 text-5xl font-bold coloredTitle">
        Welcome to svelte-tailwind-box!
    </h1>
    {#if selectedAccount}
        <p>{$selectedAccount}</p>
    {/if}
</div>

<style>
    .coloredTitle {
        background: linear-gradient(
            45deg,
            #f17c58,
            #e94584,
            rgb(19, 176, 247),
            rgb(126, 253, 253)
        );
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-size: 600% 100%;
        background-position: 0;
        animation: scrollingGradient 6s linear infinite forwards;
        animation-direction: alternate;
    }

    @keyframes scrollingGradient {
        0% {
            background-position: 0%;
        }
        100% {
            background-position: 100%;
        }
    }
</style>
