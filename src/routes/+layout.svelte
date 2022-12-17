<script>
  import Header from './Header.svelte';
  import './styles.sass';
</script>

<div class="app">
  <Header />

  <main>
    <slot />
  </main>
</div>
