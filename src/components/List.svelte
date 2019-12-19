<script>
  import Item from './Item.svelte';

  export let items = [];
</script>

{#each items as item}
  <slot {item} />
{/each}
