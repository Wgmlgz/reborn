<script>
  import BackBar from './back-bar.svelte';

  const cols = 4;
</script>

<div class="absolute -z-10 w-screen h-[500vh] bg-back overflow-clip">
  <div
    class="rotate-[2deg] -translate-x-[25vw] -translate-y-[25vh] grid grid-flow-col grid-cols-[{cols}] w-[125%]"
  >
    <div class="overflow-hidden -scale-x-100">
      <BackBar dir="normal" />
    </div>
    <div class="overflow-hidden scale-x-100">
      <BackBar dir="reverse" />
    </div>
    <div class="overflow-hidden">
      <BackBar dir="normal" />
    </div>
    <div class="overflow-hidden -scale-x-100">
      <BackBar dir="reverse" />
    </div>
    <div class="overflow-hidden -scale-x-100">
      <BackBar dir="normal" />
    </div>
    <div class="absolute w-full h-full" />

    <!-- {#each { length: cols } as _, i}
      <div class='overflow-hidden scale-x-100'>
        <BackBar dir={i % 2 ? 'normal' : 'reverse'} />
      </div>
    {/each} -->
  </div>
</div>
