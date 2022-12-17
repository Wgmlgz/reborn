<script>
  import welcome from '$lib/images/svelte-welcome.webp';
  import welcome_fallback from '$lib/images/svelte-welcome.png';
  import FloatBox from '$lib/components/float-box.svelte';
  import Frame from '$lib/components/frame.svelte';
  import Box from '$lib/components/box.svelte';
  import Boot from '$lib/components/boot.svelte';
  import Back from '$lib/components/back.svelte';

  let w = 500;
  let h = 100;

  let w1 = 500;
  let h1 = 100;

  let show = true;

  const click = () => {
    console.log('sus');
    show = false;
    setTimeout(() => {
      show = true;
    }, 0);
  };
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <div class="grid">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="grid h-screen items-center justify-center" on:click={click}>
      {#if show}
        <div class="grid relative h-min w-min">
          <Boot />
          <div
            class="absolute top-3 left-3 opacity-10 transition hover:translate-x-1 hover:translate-y-3"
          >
            <Boot />
          </div>
        </div>
      {/if}
    </div>
    <div class=" m-9">
      <p>
        Разнообразный и богатый опыт управление и развитие структуры влечёт за собой интересный
        процесс внедрения модернизации существующий финансовых и административных условий. Задача
        организации, в особенности же выбранный нами инновационный путь влечёт за собой интересный
        процесс внедрения модернизации форм воздействия. Идейные соображения высшего порядка, а
        также постоянный количественный рост и сфера нашей активности требует от нас анализа
        позиции, занимаемых участниками в отношении поставленных задач. Задача организации, в
        особенности же постоянный количественный рост и сфера нашей активности играет важную роль в
        формировании поставленных обществом и правительством задач. Равным образом новая модель
        организационной деятельности в значительной степени обуславливает создание поставленных
        обществом и правительством задач. Следует отметить, что реализация намеченных плановых
        заданий обеспечивает актуальность форм воздействия. Повседневная практика показывает, что
        управление и развитие структуры позволяет оценить значение соответствующих условий
        активизации. Не вызывает сомнений, что реализация намеченных плановых заданий обеспечивает
        актуальность дальнейших направлений развития. Равным образом выбранный нами инновационный
        путь позволяет оценить значение дальнейших направлений развития. Прежде всего
        социально-экономическое развитие создаёт предпосылки качественно новых шагов для направлений
        прогрессивного развития.
      </p>
    </div>
  </div>
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
