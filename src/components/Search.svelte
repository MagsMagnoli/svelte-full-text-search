<script>
  import { MDCTextField } from '@material/textfield/index';
  import { onMount } from 'svelte';

  export let query;
</script>

<div class="search">
  <form>
    <input bind:value={query} type="search" placeholder="Search" />
  </form>
</div>
