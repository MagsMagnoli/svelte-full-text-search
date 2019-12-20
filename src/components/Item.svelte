<script>
  export let item;
</script>

<style>
  .item {
    border: 1px solid white;
    width: 300px;
    height: 300px;
    margin: 8px;
    padding: 16px;
  }
</style>

<div class="item">
  <h1>{item.title}</h1>
  <p>{item.tags.join(', ')}</p>
  <p>{item.description}</p>
</div>
