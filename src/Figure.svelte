<script>
  export let image;
  export let i;
  let active = false

  const handleClick = (event) => active = !active
</script>

<style>
  figure {
    width: 33.33%;
    padding: 0.5rem;
    transition: transform ease 300ms;
    background-color: white;
    cursor: pointer;
  }

  figure.active {
    transform: scale(2);
    box-shadow: 0 0 1rem rgba(0, 0, 0, 0.15);
  }
</style>

<figure on:click={handleClick} class:active>
  <img src={image} />
  <figcaption>Image {i + 1}</figcaption>
</figure>