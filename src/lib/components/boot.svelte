<script lang="ts">
  0.3;
  import Box from './box.svelte';
  import { css } from 'goober';

  const n = 20;
  const p = [0.0, 0.1, 0.3, 0.45, 0.5, 0.55, 0.7, 0.95, 1.0].map((x) => x / 2);
  p.push(0.51);
  p.push(0.55);
  p.push(0.6);
  p.push(1);

  const makeAnim = (name: string, f: (p: number) => string) =>
    css`
      &:after {
        animation: ${name} 3s 1s linear 1 both;
        content: '';
        @keyframes ${name} {
          ${p
            .map((p) => `${Math.round(p * 100)}% { content: '${f(p)}';} \n`)
            .reduce((a, b) => a + b)}
        }
      }
    `;

  const a = makeAnim('loading-a', (p) => (p < 0.5 ? '#'.repeat(n * p * 2) : ''));
  const b = makeAnim('loading-b', (p) => (p < 0.5 ? '.'.repeat(n - n * p * 2) : ''));
  const c = makeAnim('loading-c', (p) => (p < 0.5 ? `${Math.round(p * 100 * 2)}%` : ''));

  const d = makeAnim('loading-d', (p) => (p < 0.5 ? '[' : ''));
  const e = makeAnim('loading-e', (p) => (p < 0.5 ? ']' : ''));
  const f = makeAnim('loading-f', (p) => (p < 0.5 ? '[ SYSTEM REBOOT ]' : ''));

  const g = makeAnim('loading-g', (p) => (p > 0.7 ? '< WGMLGZ_ >' : ''));
</script>

<Box class="p-10 m-auto">
  <div class="frame text-white">
    <div class="absolute grid justify-items-center">
      <div class="grid justify-items-center gap-2 w-[700px] -mx-[50%]">
        <p class="{f} text-4xl mt-7" />
        <p class="{g} text-8xl -mt-7" style="content: 'sus'" />
        <p class={c} />
        <div class="flex font-mono text-2xl">
          <p class={d} />
          <p class={a} />
          <p class="text-white {b}" />
          <p class={e} />
        </div>
      </div>
    </div>
  </div>
</Box>

<style lang="scss">
  @use '$lib/styles/colors.sass';

  @keyframes loading-c {
    51% {
      content: '';
    }
    60% {
      content: '';
    }
    100% {
      content: '';
    }
  }
  .frame {
    width: 700px;
    animation: myAnim 3s cubic-bezier(0.34, 1.56, 0.64, 1) 1s 1 normal both;
  }

  @keyframes myAnim {
    0% {
      min-height: 200px;
    }
    5% {
      min-height: 200px;
    }
    60% {
      min-height: 200px;
    }
    67% {
      min-height: 120px;
    }
    100% {
      min-height: 120px;
    }
  }

  div {
    // animation: border-flicker 1s linear infinite;
  }
</style>
