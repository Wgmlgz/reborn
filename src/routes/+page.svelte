<script>
  import welcome from '$lib/images/svelte-welcome.webp';
  import welcome_fallback from '$lib/images/svelte-welcome.png';
  import FloatBox from '$lib/components/float-box.svelte';
  import Frame from '$lib/components/frame.svelte';
  import Box from '$lib/components/box.svelte';
  import Boot from '$lib/components/boot.svelte';

  let w = 500;
  let h = 100;

  let w1 = 500;
  let h1 = 100;
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <Boot></Boot>
  <!-- <FloatBox>
    <div class="h-50 w-50">
      <Box bind:w bind:h>
        <div class="h-60">
          <Frame
            src="https://wgmlgz.github.io/main/"
            title="forever old"
            scale={0.1}
            w="{w}px"
            h="{h}px"
            disable={true}
          />
        </div>
      </Box>
    </div>
  </FloatBox> -->
</section>

<style lang="sass">

</style>
