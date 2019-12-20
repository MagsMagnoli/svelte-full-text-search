<script>
  export let item;
</script>

<style>
  .item-content {
    display: flex;
    flex-direction: column;
    min-height: 250px;
  }

  .description {
    flex-grow: 1;
  }

  .tag:not(:last-child) {
    margin-right: 8px;
  }
</style>

<div class="card item">
  <div class="card-content item-content">
    <span class="card-title">{item.title}</span>
    <p class="description">{item.description}</p>
    <div class="tags-container">
      {#each item.tags as tag}
        <div class="chip tag">{tag}</div>
      {/each}
    </div>
  </div>
</div>
