<script lang="ts">
  import "../app.postcss";
  import { AppShell, AppBar } from "@skeletonlabs/skeleton";
</script>

<AppShell>
  <svelte:fragment slot="header">
    <AppBar>
      <svelte:fragment slot="lead">
        <strong class="text-xl uppercase">Juan.S</strong>
      </svelte:fragment>
      <svelte:fragment slot="trail">
        <a
          class="btn btn-sm bg-blue-700"
          href="https://www.linkedin.com/in/juan-jr-sierra/"
          target="_blank"
          rel="noreferrer"
        >
          LinkedIn
        </a>
        <a
          class="btn btn-sm bg-tertiary-600"
          href="https://github.com/JuanSierra99"
          target="_blank"
          rel="noreferrer"
        >
          GitHub
        </a>
        <a
          class="btn btn-sm variant-ghost-surface"
          href="/Juan-Sierra-Resume.pdf"
          download
        >
          Resume
        </a>
      </svelte:fragment>
    </AppBar>
  </svelte:fragment>
  <slot />
</AppShell>
