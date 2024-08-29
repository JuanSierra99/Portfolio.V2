<script>
  import { Accordion, AccordionItem } from "@skeletonlabs/skeleton";
  import IconHeart from "~icons/mdi/heart";
  import IconPhone from "~icons/mdi/cellphone";
  import IconCamera from "~icons/mdi/camera";
  import IconMoney from "~icons/mdi/money-100";
  import IconDog from "~icons/mdi/dog";

  const contentStyles = "";
  const repoLinkStyles =
    "w-fit btn variant-filled-tertiary block ml-auto mr-auto mt-3";
</script>

<Accordion>
  <AccordionItem open>
    <svelte:fragment slot="lead"
      ><IconDog class="text-yellow-300" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Bucket Buddy</svelte:fragment>
    <svelte:fragment slot="content">
      <p>
        A web app that allows users to organize their life by giving them a
        simple way to create lists that can help them keep track of tasks they
        would like to complete. Bucket Buddy is designed to help individuals who
        struggle with managing their goals.
      </p>
      <div class="relative pt-5">
        <img
          src="/hanging_spot.webp"
          class="h-[50px] w-auto absolute translate-y-[-35px] right-0"
          alt="spotted dog with tounge out"
        />
        <!-- <img
          src="/hanging_bern.webp"
          class="h-[50px] w-auto absolute translate-y-[-35px] left-0"
          alt="brown dog with tounge out"
        /> -->
        <img
          src="/bucketbuddy-homepage.webp"
          class="rounded-md"
          alt="bucket buddy website homepage"
        />
        <a
          class={repoLinkStyles}
          href="https://github.com/JuanSierra99/BucketBuddy">Visit Repo</a
        >
      </div>
    </svelte:fragment>
  </AccordionItem>

  <AccordionItem>
    <svelte:fragment slot="lead">
      <IconHeart class="text-pink-300 w-5" /></svelte:fragment
    >
    <svelte:fragment slot="summary">You Will Be Mine</svelte:fragment>
    <svelte:fragment slot="content">
      <p>
        💘 Introducing "You Will Be My Valentine" - A labor of love crafted with
        Svelte. 💘 Choosing not to use any external libraries really helped in
        deepening my understanding of Svelte and its capabilities. Pressing the
        "Yes" button triggers a burst of confetti, but the magic doesn’t end
        there. Each confetti piece can be clicked, causing even more confetti to
        explode from it. It’s a celebration that keeps on giving with every
        click!
      </p>
      <img
        src="/kaboom.gif"
        class="rounded-sm w-full ml-auto mr-auto"
        alt="gif of my confetti website"
      />
      <a
        class={repoLinkStyles}
        href="https://github.com/JuanSierra99/you-will-be-mine">Visit Repo</a
      ></svelte:fragment
    >
  </AccordionItem>

  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconPhone class="text-sky-300" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Decibel Warrior</svelte:fragment>
    <svelte:fragment slot="content">
      <span class="">
        The thrilling mobile app that keeps you on your toes! Keep your finger
        within the moving radius, or face the hilarious consequence of an audio
        clip featuring a man's uproarious yelling. With a scoreboard to track
        your progress and sound customizations to fit your preferences, stay
        sharp, stay entertained, and stay on the screen with "Decibel Warrior"!
      </span>
      <img
        src="/decibel-warrior.webp"
        class="rounded-md"
        alt="decibel warrior mobile game welcome screen"
      />
      <a
        class={repoLinkStyles}
        href="https://github.com/JuanSierra99/decibel_warrior">Visit Repo</a
      >
    </svelte:fragment>
  </AccordionItem>

  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconCamera class="text-orange-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">AI Film Site</svelte:fragment>
    <svelte:fragment slot="content">
      <span class="">
        A web app for maintaining a collection of your favorite film photos. The
        custom api is built with python and uses machine learning for object
        recognition, Numpy for image masking, and openai api for image editing
        using artifical intelligence. Simple to use, and pleasent to view.
      </span>
      <img
        src="/film-website.webp"
        class="rounded-md"
        alt="film gallery website"
      />
      <a class={repoLinkStyles} href="https://github.com/JuanSierra99/Film-Site"
        >Visit Repo</a
      >
    </svelte:fragment>
  </AccordionItem>

  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconMoney class="text-green-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Accounting Website</svelte:fragment>
    <svelte:fragment slot="content">
      <span class=""> </span>
      <img
        src="/bills-invoices.gif"
        class="rounded-md"
        alt="Accounting website demo"
      />
      <a
        class={repoLinkStyles}
        href="https://github.com/JuanSierra99/Stock-Analyzer">Visit Repo</a
      >
    </svelte:fragment>
  </AccordionItem>
</Accordion>
