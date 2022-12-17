<script lang="ts">
  export let w: number = 100;
  export let h: number = 100;
  export let top = false;
</script>

<section class="draggable border-flicker  border-2 border-solid {$$restProps.class || ''}">
  {#if top}
    <div class="top">REBOOT</div>
  {/if}
  <div class="bot" bind:clientWidth={w} bind:clientHeight={h}>
    <span class="btn__glitch" />
    <slot />
  </div>
  <!-- <button class="btn">
    <span class="btn__content">Get your copy now_</span>
    <span class="btn__glitch"></span>
    <span class="btn__label">r25</span>
  </button> -->
</section>

<style lang="scss">
  @use '$lib/styles/colors.sass';
  @import url('https://fonts.googleapis.com/css?family=Barlow|Tomorrow:400,700&display=swap');

  .draggable {
    border: solid 5px rgba(colors.$primary, 0.8);
    box-shadow: 0 0 20px rgba(colors.$primary, 0.5);
    background-color: rgba(colors.$primary, 0.1);
  }
  .top {
    width: 100%;
    height: var(--bar-w);
  }
  .bot {
    width: 100%;
    top: var(--bar-w);
    bottom: 0;
  }

  .border-flicker {
    animation: border-flicker 2s linear infinite;
  }

  #offset {
    animation: letter-flicker 2s linear infinite;
  }

  @keyframes text-flicker {
    0% {
      opacity: 0.1;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    2% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    8% {
      opacity: 0.1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    9% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    12% {
      opacity: 0.1;
      text-shadow: 0px 0px colors.$primary;
    }
    20% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    25% {
      opacity: 0.3;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    30% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    70% {
      opacity: 0.7;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    72% {
      opacity: 0.2;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    77% {
      opacity: 0.9;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    100% {
      opacity: 0.9;
      text-shadow: 0px 0px 29px colors.$primary;
    }
  }

  @keyframes border-flicker {
    0% {
      opacity: 0.3;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }
    2% {
      opacity: 1;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }
    4% {
      opacity: 0.3;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }

    8% {
      opacity: 1;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }
    70% {
      opacity: 0.7;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }
    100% {
      opacity: 1;
      -webkit-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      -moz-box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
      box-shadow: 0px 0px 20px 4px rgba(colors.$primary, 0.5);
    }
  }

  @keyframes letter-flicker {
    0% {
      opacity: 0.1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    2% {
      opacity: 0.1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    4% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    19% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    21% {
      opacity: 0.1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    23% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }

    80% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    83% {
      opacity: 0.4;
      text-shadow: 0px 0px 29px colors.$primary;
    }
    87% {
      opacity: 1;
      text-shadow: 0px 0px 29px colors.$primary;
    }
  }
</style>
