<script lang="ts">
      import { Autocomplete } from "@skeletonlabs/skeleton";
      import type { AutocompleteOption } from "@skeletonlabs/skeleton";
      import { RadioGroup, RadioItem } from '@skeletonlabs/skeleton';

      let skillFilter: string = "";

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
  <div
    class=" w-full max-w-full max-h-screen overflow-y-auto"
    tabindex="-1"
  >
    <RadioGroup display="flex" >
    <RadioItem bind:group={skillFilter} name={"Filter"} value={""}>All</RadioItem>
    <RadioItem bind:group={skillFilter} name={"Filter"} value={"frontend"}>Frontend</RadioItem>
    <RadioItem bind:group={skillFilter} name={"Filter"} value={"backend"}>Backend</RadioItem>
    <RadioItem bind:group={skillFilter} name={"Filter"} value={"languages"}>Languages</RadioItem>
  </RadioGroup>
    <Autocomplete bind:input={skillFilter} options={skills} />
  </div>