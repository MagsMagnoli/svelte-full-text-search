<script>
  import Search from './Search.svelte';
  import Items from './Items.svelte';
  import Filter from './Filter.svelte';
  import List from './List.svelte';
  import Item from './Item.svelte';

  let searchQuery = '';
</script>

<Search bind:query={searchQuery} />
<Items let:items>
  <Filter {items} {searchQuery} let:filteredItems>
    <List items={filteredItems} let:item>
      <Item {item} />
    </List>
  </Filter>
</Items>
