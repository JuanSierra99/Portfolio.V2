<script>
  import { Accordion, AccordionItem } from "@skeletonlabs/skeleton";
  import IconHeart from "~icons/mdi/heart";
  import IconPhone from "~icons/mdi/cellphone";
  import IconCamera from "~icons/mdi/camera";
  import IconMoney from "~icons/mdi/money-100";
  import IconDollarSymbol from "~icons/mdi/attach-money";
  import IconDog from "~icons/mdi/dog";
  import IconStock from "~icons/mdi/chart-line";
  import IconPeople from "~icons/mdi/people-add";
  import IconRobotLove from "~icons/mdi/robot-love-outline";
  import Photos from "~icons/mdi/insert-photo";

  let accordionRef;

  const repoLinkStyles = "w-fit btn bg-tertiary-600 block ml-auto mr-auto mt-3";
</script>

<img src="/valueglance.webp" class="hidden" alt="Preload" />
<img src="/bucketbuddy-homepage.webp" class="hidden" alt="Preload" />
<img src="/hanging_spot.webp" class="hidden" alt="Preload" />
<img src="/portfolio.v1.webp" class="hidden" alt="Preload" />
<img src="/octech.webp" class="hidden" alt="Preload" />
<img src="/kaboom.gif" class="hidden" alt="Preload" />
<img src="/Bargraph.webp" class="hidden" alt="Preload" />
<img src="/bills-invoices.gif" class="hidden" alt="Preload" />
<img src="/film-website.webp" class="hidden" alt="Preload" />
<img src="/decibel-warrior.webp" class="hidden" alt="Preload" />

<Accordion>
  <!-- Value Glance -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconDollarSymbol class="text-emerald-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Value Glance</svelte:fragment>
    <svelte:fragment slot="content">
      <p>
        During my time at First Principles Publishing, I contributed to
        valueglance.com by applying my React and Tailwind skills. I made
        meaningful contributions to the product and had the opportunity to work
        closely with the design team to enhance both functionality and design.
      </p>
      <p>
        Here’s a snippet of the Manage Subscription page I implemented. This
        page is crucial for displaying users' current subscription and billing
        data and guiding them to Stripe for subscription management or
        configuration.
      </p>
      <img
        src="/valueglance.webp"
        class="rounded-md"
        alt="Accounting website demo"
      />
      <a class={repoLinkStyles} href="https://valueglance.com/">Visit Site</a>
    </svelte:fragment>
  </AccordionItem>

  <!-- Film Gallery -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><Photos class="text-orange-500" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Film Gallery</svelte:fragment>
    <svelte:fragment slot="content">
      <div class="space-y-3">
        <iframe
          src="https://www.youtube.com/embed/YoCZMrxlgOk"
          title="film gallery demo"
        >
        </iframe>
        <p>
          This project is a Svelte x Nginx website where I showcase my film
          photography in a beautiful and engaging format. While building it, I
          explored ways to improve performance when running the site locally
          without compressing or converting my original .jpg images.
        </p>
        <p>
          In this demo, I share some of the strategies I used, like loading
          low-res versions of the images during the initial load to avoid
          overwhelming the browser with high-res downloads all at once. I also
          implemented the lazy attribute on {"<img />"} elements and used Intersection
          Observer to dynamically load high-res images as they come into view.
        </p>
        <p>
          To further optimize, I configured Nginx to enable browser caching for
          the images, ensuring that they load instantly on subsequent visits.
          This combination of techniques creates a seamless experience while
          preserving the quality of my work.
        </p>
        <p>
          Finally, I explore additional possibilities, such as converting my
          images to WebP format to significantly reduce file sizes, while
          keeping it's quality, or implementing a loading screen to enhance the
          user experience while high-resolution images are being loaded.
        </p>
      </div>
      <a
        class={repoLinkStyles}
        href="https://www.youtube.com/watch?v=YoCZMrxlgOk">Youtube</a
      >
    </svelte:fragment>
  </AccordionItem>

  <!-- BUCKET BUDDY -->
  <AccordionItem bind:this={accordionRef}>
    <svelte:fragment slot="lead"
      ><IconDog class="text-yellow-300" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Bucket Buddy</svelte:fragment>
    <svelte:fragment slot="content">
      <p>
        A Fullstack project that allows users to organize their life by giving
        them a simple way to create lists that can help them keep track of tasks
        they would like to complete. Bucket Buddy is designed to help
        individuals who struggle with managing their goals. This is the recent
        redesign of the landing page, though i can't host it on my EC2 server
        right now because i can't afford to let Jeff Bezos take whatever money i
        have left.
      </p>
      <div class="relative pt-5">
        <img
          src="/hanging_spot.webp"
          class="h-[50px] w-auto absolute translate-y-[-35px] right-0"
          alt="spotted dog with tounge out"
        />
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

  <!--Portfolio V1 -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconRobotLove class="text-red-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">OG Portfolio</svelte:fragment>
    <svelte:fragment slot="content">
      <span class="">
        I wanted to stick with just HTML, CSS, and JavaScript for this one. It
        was a great learning experience, and I had so much designing it all from
        scratch. It also made me appreciate why frameworks are so
        handy—components are awesome and way more readable!
      </span>
      <img
        src="/portfolio.v1.webp"
        class="rounded-md"
        alt="decibel warrior mobile game welcome screen"
      />
      <a class={repoLinkStyles} href="https://juansierra99.github.io"
        >Visit Site</a
      >
    </svelte:fragment>
  </AccordionItem>

  <!-- OC TECH LINK UP -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconPeople class="text-[#eae2b7]" /></svelte:fragment
    >
    <svelte:fragment slot="summary">OC Tech</svelte:fragment>
    <svelte:fragment slot="content">
      <span class=""
        >Designed and developed with WordPress, this landing page features a
        stunning design and includes relevant links to connect and engage with
        the tech community in Orange County. It’s crafted to bring people
        together and foster networking within the local tech scene.
      </span>
      <img
        src="/octech.webp"
        class="rounded-md"
        alt="orange county tech meetup"
      />
      <a class={repoLinkStyles} href="https://octechlinkup.com/">Visit Site</a>
    </svelte:fragment>
  </AccordionItem>

  <!-- YOU WILL BE MINE -->
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

  <!-- STOCK ANALYZER -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconStock class="text-orange-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Stock Analyzer</svelte:fragment>
    <svelte:fragment slot="content">
      <span class=""
        >This is a financial graphing application that utilizes Vite, React, and
        Chart.js to display historical data from the AlphaVantage API. Value
        Glance was my inspiration for this project.
      </span>
      <img
        src="/Bargraph.webp"
        class="rounded-md"
        alt="Accounting website demo"
      />
      <a
        class={repoLinkStyles}
        href="https://github.com/JuanSierra99/Stock-Analyzer">Visit Repo</a
      >
    </svelte:fragment>
  </AccordionItem>

  <!-- ACCOUNTING WEBSSITE -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconMoney class="text-green-400" /></svelte:fragment
    >
    <svelte:fragment slot="summary">Accounting Website</svelte:fragment>
    <svelte:fragment slot="content">
      <span class=""
        >The primary goal of this project was to demonstrate a well-rounded
        skill set in full-stack development, encompassing both backend and
        frontend domains. The backend is engineered using Node.js with NestJS,
        integrating Prisma ORM for sophisticated data handling. The frontend,
        developed with React and enriched by TypeScript's type safety, offers a
        seamless user experience for interacting with financial records.</span
      >
      <img
        src="/bills-invoices.gif"
        class="rounded-md"
        alt="Accounting website demo"
      />
      <a
        class={repoLinkStyles}
        href="https://github.com/JuanSierra99/Accounting-Website">Visit Repo</a
      >
    </svelte:fragment>
  </AccordionItem>

  <!-- AI FILM SITE -->
  <AccordionItem>
    <svelte:fragment slot="lead"
      ><IconCamera class="text-purple-400" /></svelte:fragment
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

  <!-- DECIBEL WARRIOR -->
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
</Accordion>

<style>
  iframe {
    width: 100%;
    aspect-ratio: 16/9;
  }
</style>
