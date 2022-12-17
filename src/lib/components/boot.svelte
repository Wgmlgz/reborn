<script lang="ts">
  import Box from './box.svelte';
</script>

<div class="grid">
  <div class="grid h-screen">
    <Box class="p-10 m-auto">
      <div class="grid justify-items-center gap-9">
        <p class="text-primary text-8xl">[ Wgmlgz ]</p>
        <div class="flex font-mono text-2xl">
          <p class="">#####</p>
          <p class="text-white spin ">......</p>
        </div>
      </div>
    </Box>
  </div>
</div>

<style>
  @keyframes spin {
    0% { content:"ipsum"; }
    10% { content:"dolor"; }
    20% { content:"sit"; }
    30% { content:"amet"; }
    40% { content:"consectetur"; }
    50% { content: "adipisicing"; }
    60% { content: "elit"; }
    70% { content: "Hic"; }
    80% { content: "atque"; }
    90% { content: "fuga"; }
  }
</style>
