<script>
  import Header from './Header.svelte';
  import '$lib/styles/styles.sass';
</script>

<div class="app">
  <Header />

  <main>
    <slot />
  </main>
</div>
