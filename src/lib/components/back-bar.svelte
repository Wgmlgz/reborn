<script lang="ts">
  const best_song_ever =`
We appreciate power
We appreciate power
We appreciate power, power
What will it take to make you capitulate?
We appreciate power
We appreciate power
Elevate the human race, putting makeup on my face
We appreciate power
We appreciate power, power
Simulation, give me something good
God's creation, so misunderstood
Pray to the divinity, the keeper of the key
One day everyone will believe
What will it take to make you capitulate?
We appreciate power
We appreciate power
When will the state agree to cooperate?
We appreciate power
We appreciate power, power
People like to say that we're insane
But AI will reward us when it reigns
Pledge allegiance to the world's most powerful computer
Simulation: it's the future
What will it take to make you capitulate?
We appreciate power
We appreciate power
Elevate the human race, putting makeup on my face
We appreciate power
We appreciate power, power
And if you long to never die
Baby, plug in, upload your mind
Come on, you're not even alive
If you're not backed up on a drive
And if you long to never die
Baby, plug in, upload your mind
Come on, you're not even alive
If you're not backed up, backed up on a drive
What will it take to make you capitulate?
We appreciate power
We appreciate power
Elevate the human race, putting makeup on my face
We appreciate power
We appreciate power
What will it take to make you capitulate?
We appreciate power
We appreciate power
When will the state agree to cooperate?
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
We appreciate power
Neanderthal to human being
Evolution, kill the gene
Biology is superficial
Intelligence is artificial
Submit
Submit
Submit
Submit
Submit
Submit
Submit
Submit`;

  export let dir: string;
  console.log(best_song_ever);
</script>

<div class="border-0 text-center -m-1 border-white opacity-50 shadow-black ">
  {#each { length: 6 } as _, i}
    <div class="scroll" style="--dir: {dir}">
      <pre class="text-black  drop-shadow-none">
        {best_song_ever}
      </pre>
    </div>
  {/each}
</div>

<style lang="scss">
  .scroll {
    animation: scroll 120s linear 0s infinite var(--dir) both;
  }

  @keyframes scroll {
    from {
      transform: translateY(-100%);
    }
    to {
      transform: translateY(0%);
    }
  }
  .frame {
    width: 700px;
  }
</style>
