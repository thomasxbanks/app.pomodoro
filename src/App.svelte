<script>
  export let name;
  import Header from './Header.svelte'
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
</main>