<script>
import '../../css/index.css'

import PageLoader from './PageLoader.svelte'

export let data
</script>

<svelte:head>
  <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
  <link rel="alternate" type="application/rss+xml" title="RSS" href="/feed.xml" />
  <!-- Analytics for Demo Website; you can safely remove this section -->
  {#if data.host === 'tablogdemo.vercel.app'}<script
      defer
      data-domain="tablogdemo.vercel.app"
      src="https://plausible.io/js/script.js"
    ></script>{/if}
</svelte:head>

<PageLoader />

<div class="minvh mindvh col max49 mx">

  <main class="span1">
    <slot />
  </main>

   

</div>