<script lang="ts">
  export let left = 100;
  export let top = 100;

  let moving = false;

  const onMouseDown = () => (moving = true);
  const onMouseUp = () => (moving = false);
  const onMouseMove = ({ movementX, movementY }: MouseEvent) => {
    if (moving) {
      left += movementX;
      top += movementY;
    }
  };
</script>

<section
  on:mousedown={onMouseDown}
  style="left: {left}px; top: {top}px;"
  class="select-none cursor-move absolute"
>
  <slot />
</section>

<svelte:window on:mouseup={onMouseUp} on:mousemove={onMouseMove} />
