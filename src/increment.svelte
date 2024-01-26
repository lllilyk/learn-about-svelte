<script>
    import { count } from './stores.js'

    const onIncre = () => {
        $count = $count + 1;
    }
</script>

<button on:click={onIncre}>+</button>