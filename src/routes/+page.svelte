<script lang="ts">
  import { Avatar } from "@skeletonlabs/skeleton";
  import Projects from "$lib/Projects.svelte";
  import Skills from "$lib/Skills.svelte";
  import Education from "$lib/Education.svelte";
</script>

  <div class="container mx-auto p-8 space-y-8 max-w-3xl">
    <div class="flex w-full justify-between items-center">
      <h1 class="h1">
        <span class=""> Juan </span>
      </h1>
      <Avatar src="/juan.png" class="inline" />
    </div>
    <p>
      <strong class="text-gray-400">1</strong> A fullstack developer navigating the
      complex yet beautiful world of web development.
    </p>
    <h2 class="font-bold text-3xl">Skills</h2>
    <Skills />
    <h2 class="font-bold text-3xl">Projects</h2>
    <Projects />
    <h2 class="font-bold text-3xl">Education</h2>
    <Education />
  </div>
