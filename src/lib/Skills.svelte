<script lang="ts">
  import { Autocomplete } from "@skeletonlabs/skeleton";
  import type { AutocompleteOption } from "@skeletonlabs/skeleton";
  import IconClear from "~icons/mdi/clear-bold";

  let skillFilter: string = "";

  const skills: AutocompleteOption<string>[] = [
    {
      label: "Javascript",
      value: "javascript",
      keywords: "frontend, backend",
    },
    {
      label: "Python",
      value: "python",
      keywords: "backend",
    },
    {
      label: "Java",
      value: "java",
      keywords: "backend",
    },
    {
      label: "C++",
      value: "c++",
      keywords: "backend",
    },
    {
      label: "NodeJs",
      value: "nodejs",
      keywords: "backend",
    },
    {
      label: "JSON",
      value: "json",
      keywords: "frontend, backend",
    },
    {
      label: "Express",
      value: "express",
      keywords: "backend",
    },
    {
      label: "React",
      value: "react",
      keywords: "frontend",
    },
    {
      label: "Svelte",
      value: "svelte",
      keywords: "frontend",
    },
    {
      label: "SvelteKit",
      value: "sveltekit",
      keywords: "frontend, backend",
    },
    {
      label: "HTML",
      value: "html",
      keywords: "frontend",
    },
    {
      label: "CSS",
      value: "css",
      keywords: "frontend",
    },
    {
      label: "Tailwind",
      value: "tailwind",
      keywords: "frontend",
    },
    {
      label: "Postgres",
      value: "postgres",
      keywords: "backend",
    },
    {
      label: "MySql",
      value: "mysql",
      keywords: "backend",
    },
    {
      label: "NGINX",
      value: "nginx",
      keywords: "backend",
    },
    {
      label: "EC2",
      value: "ec2",
      keywords: "backend",
    },
    {
      label: "Netlify",
      value: "netlify",
      keywords: "backend",
    },
    {
      label: "Git",
      value: "git",
      keywords: "",
    },
    {
      label: "Github",
      value: "github",
      keywords: "",
    },
    {
      label: "Stripe",
      value: "stripe",
      keywords: "backend",
    },
  ];
</script>

<div
  class=" w-full max-w-full max-h-screen overflow-y-auto card p-4"
  tabindex="-1"
>
  <div class="mb-1">
    <button
      class="btn variant-form-material text-xs hover:border-tertiary-600"
      on:click={() => {
        skillFilter = "Frontend";
      }}>Frontend</button
    >
    <button
      class="btn variant-form-material text-xs hover:border-tertiary-600"
      on:click={() => {
        skillFilter = "Backend";
      }}>Backend</button
    >
  </div>

  <div class="relative flex items-center variant-ghost-surface rounded-md mb-2">
    <input
      class="w-full p-2 bg-transparent hover:outline-none focus:outline-none"
      placeholder="Search..."
      bind:value={skillFilter}
    />
    <button
      class="hover:text-red-400 h-fit mr-2"
      on:click={() => {
        skillFilter = "";
      }}
    >
      <IconClear />
    </button>
  </div>
  <Autocomplete
    bind:input={skillFilter}
    options={skills}
    regionItem="w-fit text-lg hover:scale-110 hover:text-tertiary-500"
    regionList="flex flex-wrap gap-4"
    transitions={false}
  />
</div>
