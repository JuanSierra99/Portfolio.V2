<script lang="ts">
      import { Autocomplete } from "@skeletonlabs/skeleton";
      import type { AutocompleteOption } from "@skeletonlabs/skeleton";
      let inputDemo = "";

const flavorOptions: AutocompleteOption<string>[] = [
  {
    label: "Javascript",
    value: "javascript",
    keywords: "languages, frontend, backend",
    meta: { healthy: false },
  },
  {
    label: "Python",
    value: "python",
    keywords: "languages, backend",
    meta: { healthy: true },
  },
  {
    label: "Java",
    value: "java",
    keywords: "languages, backend",
    meta: { healthy: false },
  },
  {
    label: "C++",
    value: "c++",
    keywords: "backend",
    meta: { healthy: true },
  },
  {
    label: "React",
    value: "react",
    keywords: "frontend",
    meta: { healthy: true },
  },
  {
    label: "Svelte",
    value: "svelte",
    keywords: "frontend",
    meta: { healthy: true },
  },
  {
    label: "HTML",
    value: "html",
    keywords: "frontend",
    meta: { healthy: false },
  },
  {
    label: "CSS",
    value: "css",
    keywords: "frontend",
    meta: { healthy: true },
  },
  {
    label: "Tailwind",
    value: "tailwind",
    keywords: "frontend",
    meta: { healthy: false },
  },
  {
    label: "Sql",
    value: "sql",
    keywords: "database, postgres",
    meta: { healthy: false },
  },
  {
    label: "NGINX",
    value: "nginx",
    keywords: "backend, server",
    meta: { healthy: false },
  },
];

function onFlavorSelection(
  event: CustomEvent<AutocompleteOption<string>>
): void {
  inputDemo = event.detail.label;
}
</script>

<input
    class="w-full bg-transparent border-purple-400 border p-4 rounded-3xl"
    type="search"
    name="demo"
    bind:value={inputDemo}
    placeholder="Search..."
  />
  <!-- <p>
    Hint: Try typing any of the following, backend, frontend, languages,
    database
  </p> -->
  <div
    class=" w-full justify-around max-w-full max-h-screen p-4 overflow-y-auto"
    tabindex="-1"
  >
    <Autocomplete bind:input={inputDemo} options={flavorOptions} />
    <!-- <Autocomplete bind:input={inputDemo} options={techOptions2} /> -->
  </div>