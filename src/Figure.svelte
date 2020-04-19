<script>
  export let image;
  export let i = -1;
  export let hero = false;
  let active = false

  const handleClick = (event) => active = !active
</script>

<style>
  figure {
    width: 100%;
    transition: transform ease 300ms;
    background-color: white;
    cursor: pointer;
  }

  figure:not(.hero) {
    width: 33.33%;
    padding: 0.5rem;
  }

  figure.active {
    transform: scale(2);
    box-shadow: 0 0 1rem rgba(0, 0, 0, 0.15);
  }
</style>

<figure on:click={handleClick} class:hero class:active>
  <img src={image} />
  {#if i + 1 > 0}
  <figcaption>Image {i + 1}</figcaption>
  {/if}
</figure>