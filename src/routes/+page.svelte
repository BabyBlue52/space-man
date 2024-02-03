<script>
  import App from '$lib/components/App.svelte'
  import '$lib/styles.scss'
</script>

<div>
  <App />
</div>

<style>
  :global(body) {
    margin: 0;
  }

  div {
    width: 100vw;
    height: 100vh;
    background:inherit;
  }
</style>
