<script>
  import { fade, blur, fly, slide, scale, draw } from 'svelte/transition';
  import { bounceInOut, backOut } from 'svelte/easing';

  let visibles = {
    'fade': false,
    'slide': false,
    'blur': false,
    'fly': false,
    'scale': false,
  }

  const changeVisible = (type) => {
    visibles[type] = !visibles[type]
  }

</script>

<button on:click={() => changeVisible('fade')}>fade</button>
<button on:click={() => changeVisible('slide')}>slide</button>
<button on:click={() => changeVisible('blur')}>blur</button>
<button on:click={() => changeVisible('fly')}>fly</button>
<button on:click={() => changeVisible('scale')}>scale</button>

<br />

{#if visibles.fade}
  <div transition:fade={{duration:2000, delay:1000}} class="wrap">
    <h1>fade 예제</h1>
  </div>
{/if}

{#if visibles.slide}
  <div transition:slide={{easing:bounceInOut}} class="wrap">
    <h1>slide 예제</h1>
  </div>
{/if}

{#if visibles.blur}
  <div transition:blur={{opacity:100, amount:100}} class="wrap">
    <h1>blur 예제</h1>
  </div>
{/if}

{#if visibles.fly}
  <div transition:fly={{y:100, x:200, opacity:50}} class="wrap">
    <h1>fly 예제</h1>
  </div>
{/if}

{#if visibles.scale}
  <div transition:scale={{start:10}} class="wrap">
    <h1>scale 예제</h1>
  </div>
{/if}