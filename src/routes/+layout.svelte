<script lang="ts">
	import '../app.css';
	import Header from '../components/Header.svelte';

	let { children } = $props();
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous">
  <link href="https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,300..900;1,300..900&display=swap" rel="stylesheet">
</svelte:head>

<style>
  .dotted { 
    background-image: radial-gradient(circle at 1px 1px, rgb(170, 170, 170) 1px, transparent 0);
    background-size: 65px 65px;
  }

  :global(.red-hat-display) {
  font-family: "Red Hat Display", sans-serif;
  font-optical-sizing: auto;
  font-weight: 700;
  font-style: normal;
  }
</style>

<div>
<Header />

<div class='dotted m-5'>
  <div class="container mx-auto">
  {@render children()}
  </div>
</div>

<footer class="bg-muted/50">
  <div class="container py-8 mx-auto">
    <div class="flex flex-col sm:flex-row justify-between items-center space-y-4 sm:space-y-0">
      <div class="flex items-center space-x-2">
        <span class="text-2xl red-hat-display">imk.</span>
      </div>
      <p class="text-sm text-muted-foreground">© 2025 Marco Dabon. All rights reserved.</p>
    </div>
  </div>
</footer>
</div>
