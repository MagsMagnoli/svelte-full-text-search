<script>
  import Item from './Item.svelte';

  export let items = [];
</script>

<style>
  .list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    padding: 8px;
  }
</style>

<div class="list">
  {#each items as item}
    <slot {item} />
  {/each}
</div>
