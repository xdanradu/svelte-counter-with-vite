<script lang="ts">
    import { count } from '../state/counter.js';

    const decrement = () => {
        count.update(n => n - 1);
    }
</script>

<button on:click={decrement}>DECREMENT
</button>
