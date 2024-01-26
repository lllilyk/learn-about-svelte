<script>
    import { count } from './stores.js';

    const onDecre = () => {
        $count = $count - 1;
    }
</script>

<button on:click={onDecre}>-</button>