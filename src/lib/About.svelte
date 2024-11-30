<script>
  import { fade } from "svelte/transition";
  import Image from "./Image.svelte";
  let val = "traits";
</script>

<div>
  <div class="flex w-full gap-2 sm:gap-4 mb-4 font-bold">
    <label
      class="variant-glass-surface active:scale-105 {val === 'traits'
        ? 'text-tertiary-400'
        : ''}"
      for="traits"
      >Traits<input
        type="radio"
        id="traits"
        name="about"
        bind:group={val}
        value="traits"
      /></label
    >
    <label
      class="variant-glass-surface active:scale-105 {val === 'hobbies'
        ? 'text-tertiary-400'
        : ''}"
      for="hobbies"
      >Hobbies<input
        type="radio"
        id="hobbies"
        name="about"
        bind:group={val}
        value="hobbies"
      /></label
    >
  </div>

  {#if val === "traits"}
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4" in:fade>
      <Image
        src="blue-flowers.jpeg"
        alt="A film photo of blue flowers"
        title="Film photo of blue flowers"
        text="Film photography is a passion of mine. I try to capture moments and things that i find to be beautiful."
      />

      <Image
        src="puppy.jpeg"
        alt="A small brown dog laying down in the grass. It has short fur, and it is layind down next to a chewed plastic bottle."
        title="oaxca dog"
        text="I hold a special place in my heart for animals, and I have rescued several dogs throughout the years. A moment I am grateful for is being able to play fetch with a stray pup I met in Mexico."
      />
      <Image
        src="ice-cream.jpeg"
        alt="Holding up an ice cream cone"
        title="i scream for ice cream"
        text="I love traveling, ice cream, and spending time with my family. It's such a great feeling when all that is combined into one moment."
      />
      <Image
        src="garden.jpeg"
        alt="A path down a botanical garden"
        title="walking down the botanical garden"
        text="I find peace in nature, especially national parks. I love listening to the chirps of birds and smelling the plants around me, especially after a rainy day."
      />
    </div>
  {/if}

  {#if val === "hobbies"}
    <ul id="hobbies" class="space-y-4" in:fade>
      <li>
        <h3 class="text-tertiary-400 text-lg">Tech 👨‍💻</h3>
        <p>
          I am obsessed with tech, from building computers to customizing
          keyboards or collecting tech gadgets like cameras, drones, speakers,
          and microphones. Even as a kid, I loved watching videos about the
          latest iPhone leaks or reviews of the newest changes in iOS betas. To
          this day, I’m still fascinated by reading about software updates,
          patch notes, and watching everything evolve right before my eyes.
        </p>
      </li>
      <li>
        <h3 class="text-tertiary-400 text-lg">Exploring 🥾</h3>
        <p>
          Whether it’s camping in Yosemite during winter and feeling like I’m
          going to freeze to death, or going to Sequoia and stumbling into an
          angry swarm of wasps, I truly enjoy the great outdoors. Fortunately, I
          also have positive memories of being out in the wild, like finally
          seeing my first bear on my most recent trip to Sequoia! Or being able
          to go on gorgeous hikes and gaze upon the stars.
        </p>
      </li>
      <li>
        <h3 class="text-tertiary-400 text-lg">Fitness 🏋️‍♀️</h3>
        <p>
          I always feel proud after a gym session, and I try to go as frequently
          as possible. I go to stay fit and to live a healthier lifestyle. Some
          of my favorite exercises are the bench press, leg press, and stair
          master.
        </p>
      </li>
      <li>
        <h3 class="text-tertiary-400 text-lg">Family Time 💕</h3>
        <p>
          I enjoy spending time with my family, especially if it’s a movie
          night, game night, or maybe a karaoke night! My family has supported
          me through so much, and I won’t hesitate to pay it forward once I’m in
          a more fortunate position.
        </p>
      </li>
      <li>
        <h3 class="text-tertiary-400 text-lg">Gaming 🃏</h3>
        <p>
          Some video game genres I am really into are roguelikes, strategy,
          co-op, role-playing games, and survival games. Some of my favorites
          throughout the years have been
          <i>Baldur's Gate 3</i>, <i>Halo Wars 2</i>, <i>Binding of Isaac</i>,
          <i>Bloons TD 6</i>, <i>God of War</i>, <i>Black Ops 3 Zombies</i>, and
          <i>Vampire Survivors</i>. The first gaming device I ever had was a
          Game Boy, where I would play games like <i>Donkey Kong</i>, but now I
          am gaming on a PC.
        </p>
      </li>
    </ul>
  {/if}
</div>

<style>
  label {
    width: 100%;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
  }

  input[type="radio"] {
    display: none;
  }
</style>
