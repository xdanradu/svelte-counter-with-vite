<script lang="ts">
    import { count } from '../state/counter.js';

    const increment = () => {
        count.update(n => n + 1);
    }
</script>

<button on:click={increment}>INCREMENT
</button>
