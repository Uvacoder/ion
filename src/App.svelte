<script lang="ts">
  import Empty from "./views/Empty.svelte"
  import SearchBar from "./components/SearchBar.svelte"

  let projectName: string = "Ion"
</script>

<style>
  main {
    min-height: 100vh;
  }
  .explorer {
    min-height: 100vh;
    width: 45%;
    padding: 0 2rem;
    position: relative;
    background: no-repeat fixed url("../images/background.jpg");
    background-size: cover;
    background-position: center;
  }
  .explorer::after {
    content: "";
    position: absolute;
    display: block;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    backdrop-filter: blur(20px) brightness(80%);
  }
  :global(.explorer *) {
    z-index: 1;
  }
  .explorer-header {
    margin-top: 2rem;
    font-size: 1rem;
    font-weight: 700;
  }
</style>

<main class="row">
  <div class="explorer">
    <SearchBar style="margin-top: 2rem;" />
    <span class="explorer-header">{projectName}</span>
  </div>

  <Empty />
</main>
