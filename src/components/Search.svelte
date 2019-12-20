<script>
  export let query;
</script>

<form>
  <div class="input-field">
    <i class="material-icons prefix">search</i>
    <input id="search" bind:value={query} type="text" placeholder="Search" />
  </div>
</form>
