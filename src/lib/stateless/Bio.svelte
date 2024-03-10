<script>
    import AsciiA from "./ASCII_A.svelte";
</script>

<div class="bio">
    <AsciiA />
    <div class="details">
        <ul>
            <li>Name: Arjun H</li>
            <li>Job: Developer</li>
            <li>GitHub: https://github.com/J-Sparr0w</li>
            <li>Country: India</li>
        </ul>
    </div>
</div>

<style>
    .bio {
        font-size: 0.8em;
        display: flex;
    }
    .details {
        margin-top: 10px;
    }
    .details ul {
        list-style-type: none;
    }
</style>
