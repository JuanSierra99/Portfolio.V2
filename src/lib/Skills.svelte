<script lang="ts">
      import { Autocomplete } from "@skeletonlabs/skeleton";
      import type { AutocompleteOption } from "@skeletonlabs/skeleton";
      import { RadioGroup, RadioItem } from '@skeletonlabs/skeleton';

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
];
</script>
  <div
    class=" w-full max-w-full max-h-screen overflow-y-auto card p-4"
    tabindex="-1"
  >
    <RadioGroup display="flex" class={"mb-2"} >
    <RadioItem bind:group={skillFilter} name={"Filter"} value={""}>All</RadioItem>
    <RadioItem bind:group={skillFilter} name={"Filter"} value={"frontend"}>Frontend</RadioItem>
    <RadioItem bind:group={skillFilter} name={"Filter"} value={"backend"}>Backend</RadioItem>
  </RadioGroup>
    <Autocomplete bind:input={skillFilter} options={skills} regionItem="w-fit text-lg" regionList="flex flex-wrap gap-4" transitions={false}/>
  </div>
