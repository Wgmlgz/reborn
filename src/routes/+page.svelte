<script>
  import Counter from './Counter.svelte';
  import welcome from '$lib/images/svelte-welcome.webp';
  import welcome_fallback from '$lib/images/svelte-welcome.png';
  import FloatBox from '$lib/components/float-box.svelte';
  import Frame from '$lib/components/frame.svelte';

  let w = 500;
  let h = 100;
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <!-- <FloatBox>Wgmlgz</FloatBox> -->

  <FloatBox bind:w bind:h>
    <Frame
      src="https://wgmlgz.github.io/main/"
      title="forever old"
      scale={0.1}
      w="{w}px"
      h="{h}px"
    />
  </FloatBox>
</section>
