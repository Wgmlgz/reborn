<script>
  import Header from './Header.svelte';
  import '$lib/styles/styles.sass';
  import Back from '$lib/components/back.svelte';
</script>

<div class="app">
  <Back />

  <Header />

  <main>
    <slot />
  </main>
</div>
