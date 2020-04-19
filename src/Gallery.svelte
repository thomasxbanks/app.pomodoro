<script>
  export let images;
  import Figure from './Figure.svelte'
</script>
<style>
  section {
    display: flex;
    flex-wrap: wrap;
    margin: -0.5rem;
  }

  section>* {
    margin: 0.5rem;
  }

  section>h2 {
    flex-basis: 100%;
  }
</style>

<section>
  <h2>Gallery</h2>
  {#each images as image, i}
    <Figure {image} {i} />
  {:else}
    Loading...
  {/each}
</section>