<script>
  import Search from './Search.svelte';
  import Items from './Items.svelte';
  import Filter from './Filter.svelte';
  import List from './List.svelte';
  import Item from './Item.svelte';

  let searchQuery = '';
</script>

<style>
  .search-container {
    text-align: center;
    padding: 16px 16px 0 16px;
  }

  .list-container {
    display: flex;
    justify-content: center;
  }
</style>

<div class="search-container">
  <Search bind:query={searchQuery} />
</div>
<Items let:items>
  <Filter {items} {searchQuery} let:filteredItems>
    <div class="list-container">
      <List items={filteredItems} let:item>
        <Item {item} />
      </List>
    </div>
  </Filter>
</Items>
