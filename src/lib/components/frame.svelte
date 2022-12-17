<script lang="ts">
    import { stringify } from "postcss";


  export let src: string;
  export let title: string;

  export let scale: number;
  export let w: string;
  export let h: string;
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <div class="wrap" style="--scale: {scale}; --w: {w}; --h: {h}">
    <iframe class="scaled-frame" {src} {title} />
  </div>
</section>

<style lang="scss">
  .wrap {
    width: var(--w);
    height: var(--h);
    padding: 0;
    overflow: hidden;
  }
  .scaled-frame {
    width: calc(var(--w) * (1 / var(--scale)));
    height: calc(var(--h) * (1 / var(--scale)));
    border: 0px;
  }
  .scaled-frame {
    zoom: var(--scale);
    transform: scale(var(--scale));
    transform-origin: 0 0;
  }
  @media screen and (-webkit-min-device-pixel-ratio: 0) {
    .scaled-frame {
      zoom: 1;
    }
  }
</style>
