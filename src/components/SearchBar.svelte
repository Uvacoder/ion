<script lang="ts">
  import Search from "./Search.svelte"

  export let value: string = ""
  export let style: string = ""
</script>

<style>
  .search {
    display: flex;
    flex-direction: row;
    background: no-repeat fixed rgba(124, 124, 124, 0.1);
    border-radius: 10px;
  }
  input {
    background: none;
    border: none;
    outline: none;
    padding: 0.6rem 0rem;
  }
  input::placeholder {
    color: var(--text-secondary);
  }
</style>

<div class="search" {style}>
  <Search style="fill: #c9c9c9; height: 1.2rem; margin: auto 0.5rem;" />
  <input type="text" bind:value placeholder="Search code..." />
</div>
