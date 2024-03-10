<script lang="ts">
    import Bio from "./stateless/Bio.svelte";
    import TerminalTitleBar from "./TerminalTitleBar.svelte";
    import CmdInput from "./CmdInput.svelte";
</script>

<div class="terminal">
    <TerminalTitleBar />
    <Bio />
    <CmdInput />
</div>

<style>
    .terminal {
        padding-inline: 5px;
        width: 650px;
        height: 450px;
        background-color: var(--primary-color);
        border-radius: 8px;
    }
</style>
