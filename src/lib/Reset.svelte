<script lang="ts">
    import { count } from '../state/counter.js';

    const reset = () => {
        count.update(_ => 0);
    }
</script>

<button on:click={reset}>RESET
</button>

<style>
    button {
        border:3px solid navy;
    }
</style>
