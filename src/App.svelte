<script>
  export let name;
  import { onMount } from 'svelte';
  import Header from './Header.svelte'
  import Gallery from './Gallery.svelte'
  let galleryImages = [];

  onMount(() => {
    setTimeout(() => {
      galleryImages = [
        'https://picsum.photos/1024/768?random=1',
        'https://picsum.photos/1024/768?random=2',
        'https://picsum.photos/1024/768?random=3',
        'https://picsum.photos/1024/768?random=4',
        'https://picsum.photos/1024/768?random=5',
        'https://picsum.photos/1024/768?random=6',
        'https://picsum.photos/1024/768?random=7',
        'https://picsum.photos/1024/768?random=8',
        'https://picsum.photos/1024/768?random=9',
      ];
    }, 3000)
  })
</script>

<style>
  main {
    max-width: 67ch;
    margin-right: auto;
    margin-left: auto;
    padding: 1rem;
  }

  main>*+* {
    margin-top: 1.5em;
  }
</style>

<Header hero={true} {name} />
<main>
  <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Officiis nam totam dolore, eaque, quo veniam nihil delectus atque dicta esse, quibusdam earum ratione omnis. Distinctio voluptatum minus error reiciendis architecto!</p>
  <Gallery images={galleryImages} />
</main>