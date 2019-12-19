<script>
  export let items = [];
  export let searchQuery;

  function filterItems(searchQuery) {
    let filteredItems = items;

    if (!searchQuery) {
      return filteredItems;
    }

    const searchTerms = searchQuery.split(' ');

    searchTerms.forEach((term, idx) => {
      filteredItems = filteredItems.filter(item =>
        isIncluded(item, term.toLowerCase()),
      );
    });

    return filteredItems;
  }

  function isIncluded(item, term) {
    return (
      item.title.toLowerCase().includes(term) ||
      item.description.toLowerCase().includes(term) ||
      item.tags.includes(term)
    );
  }
</script>

<slot filteredItems={filterItems(searchQuery)} />
