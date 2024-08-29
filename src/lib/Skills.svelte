<script lang="ts">
      import { Autocomplete } from "@skeletonlabs/skeleton";
      import type { AutocompleteOption } from "@skeletonlabs/skeleton";
      let inputDemo = "";

const skills: AutocompleteOption<string>[] = [
  {
    label: "Javascript",
    value: "javascript",
    keywords: "languages, frontend, backend",
  },
  {
    label: "Python",
    value: "python",
    keywords: "languages, backend",
  },
  {
    label: "Java",
    value: "java",
    keywords: "languages, backend",
  },
  {
    label: "C++",
    value: "c++",
    keywords: "backend",
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
    label: "Sql",
    value: "sql",
    keywords: "database, postgres",
  },
  {
    label: "NGINX",
    value: "nginx",
    keywords: "backend, server",
  },
];
</script>

<h2 class="font-bold text-3xl">Skills</h2>
<input
    class="w-full bg-transparent border-purple-400 border p-4 rounded-3xl"
    type="search"
    name="demo"
    bind:value={inputDemo}
    placeholder="Search..."
  />
  <div
    class=" w-full justify-around max-w-full max-h-screen p-4 overflow-y-auto"
    tabindex="-1"
  >
    <Autocomplete bind:input={inputDemo} options={skills} />
  </div>