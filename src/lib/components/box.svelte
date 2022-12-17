<script lang="ts">
  export let w: number = 100;
  export let h: number = 100;
  export let top = false;
</script>

<section class="draggable border-2 border-solid {$$restProps.class || ''}">
  {#if top}
    <div class="top">REBOOT</div>
  {/if}
  <div class="bot" bind:clientWidth={w} bind:clientHeight={h}>
    <slot />
  </div>
</section>

<style lang="sass">
  @use "$lib/styles/colors.sass"

  .draggable 
    border: solid 5px rgba(colors.$primary, .8)
    box-shadow:0 0 20px rgba(colors.$primary, .5)
    background-color:  rgba(colors.$primary, .1)

  .top 
    width: 100%
    height: var(--bar-w)
  
  .bot 
    width: 100%
    top: var(--bar-w)
    bottom: 0

</style>
