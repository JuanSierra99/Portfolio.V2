<script lang="ts">
  import { Avatar } from "@skeletonlabs/skeleton";
  import Projects from "$lib/Projects.svelte";
  import Skills from "$lib/Skills.svelte";
</script>

<div class="container mx-auto p-8 space-y-8">
  <div class="flex w-full justify-between items-center">
    <h1 class="h1">Juan</h1>
    <Avatar src="/juan.png" class="inline" />
  </div>
  <p>
    <strong class="text-gray-400">1</strong> A fullstack developer navigating the
    complex yet beautiful world of web development.
  </p>
  <!-- <p>
    <strong class="text-gray-400">2</strong>
    A first-generation Mexican-American who graduated with distinction from Cal State
    University, Fullerton, earning a degree in computer science and showcasing a
    deep passion for the field.
  </p> -->
  <h2 class="font-bold text-3xl">Skills</h2>
  <Skills/>
  <h2 class="font-bold text-3xl">Projects</h2>
  <Projects/>
</div>
