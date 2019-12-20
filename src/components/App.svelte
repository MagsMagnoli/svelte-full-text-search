<script>
  import Search from './Search.svelte';
  import Items from './Items.svelte';
  import Filter from './Filter.svelte';
  import List from './List.svelte';
  import Item from './Item.svelte';

  let searchQuery = '';
</script>

<style>
  header {
    margin-top: 56px;
    text-align: center;
  }
</style>

<div class="container">
  <header>
    <h1>Full Text Search</h1>
  </header>
  <div class="search-container">
    <div class="row">
      <div class="col s12 m6 offset-m3 l4 offset-l4">
        <Search bind:query={searchQuery} />
      </div>
    </div>
  </div>
  <Items let:items>
    <Filter {items} {searchQuery} let:filteredItems>
      <div class="row">
        <List items={filteredItems} let:item>
          <div class="col s12 m6 l4">
            <Item {item} />
          </div>
        </List>
      </div>
    </Filter>
  </Items>
</div>
