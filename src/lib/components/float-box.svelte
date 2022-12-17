<script lang="ts">
  export let left = 100;
  export let top = 100;

  let moving = false;
  export let w: number;
  export let h: number;

  function onMouseDown() {
    moving = true;
  }

  function onMouseMove(e: MouseEvent) {
    if (moving) {
      left += e.movementX;
      top += e.movementY;
    }
  }

  function onMouseUp() {
    moving = false;
  }
</script>

<section
  on:mousedown={onMouseDown}
  style="left: {left}px; top: {top}px;"
  class='draggable border-2 border-solid w-[400px] h-[225px]
  transition ease-in-out hover:translate-y-1 scale-95 hover:scale-100
  '
>
  <div class="top">REBOOT</div>
  <div class="cover" />
  <div class="bot" bind:clientWidth={w} bind:clientHeight={h}>
    <slot />
  </div>
</section>

<svelte:window on:mouseup={onMouseUp} on:mousemove={onMouseMove} />

<style lang="sass">
  $primary: #ff5555
  .draggable 
    --bar-w: 20px
    user-select: none
    cursor: move
    border: solid 5px rgba($primary, .8)
    position: absolute
    box-shadow:0 0 30px rgba($primary, .5)
    background-color:  rgba($primary, .5)

  .cover
    position: absolute
    top: 0
    left: 0
    width: 100%
    height: 100%
    z-index: 100
      
  .top 
    width: 100%
    height: var(--bar-w)
  
  .bot 
    width: 100%
    position: absolute
    top: var(--bar-w)
    bottom: 0

</style>
