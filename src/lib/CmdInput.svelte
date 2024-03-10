<script lang="ts">
    import BreadCrumb from "./BreadCrumb.svelte";
    let input = "";
    let hasSubmitted = false;
    function onSubmit(e: Event) {
        hasSubmitted = true;
        if (e.target) (e.target as HTMLInputElement).disabled = true;
    }
</script>

<div class="input-wrapper">
    <div class="breadCrumbs">
        <BreadCrumb />
    </div>
    <input type="text" bind:value={input} on:change={onSubmit} />
</div>
{#if hasSubmitted}
    <div class="cmd-display">
        {input}
        <div class="time">
            {new Date().toLocaleTimeString()}
        </div>
    </div>
{/if}

<style>
    .breadCrumbs {
    }

    .input-wrapper {
        display: flex;
    }

    .cmd-display {
        padding-inline: 5px;
        margin-top: 5px;
        font-size: 0.8em;
        display: flex;
        justify-content: space-between;
    }
    .time {
        font-size: 0.7rem;
    }

    input {
        margin-left: 5px;
        width: 100%;
        outline: none;
        border: none;
        background-color: transparent;
    }

    input:disabled {
        color: var(--primary-font-color);
    }
</style>
