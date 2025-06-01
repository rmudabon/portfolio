<script lang="ts">
	import { AppBar } from '@skeletonlabs/skeleton-svelte';
	import '../app.css';
	import LightSwitch from '../components/LightSwitch.svelte';
	import { Download, Menu } from '@lucide/svelte';

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

  .red-hat-display {
  font-family: "Red Hat Display", sans-serif;
  font-optical-sizing: auto;
  font-weight: 700;
  font-style: normal;
  }
</style>

<div>
<AppBar classes='bg-transparent/95 sticky top-0 z-50 backdrop-blur' headlineClasses="sm:hidden" centerClasses="flex items-center justify-center">
  {#snippet lead()}
  <a href="/" class="btn">
    <span class="text-2xl red-hat-display">imk.</span>
  </a>
  {/snippet}
  {#snippet trail()}
    <div class='hidden sm:flex items-center gap-4'>
      <button class="bg-linear-to-bl from-violet-500 to-fuchsia-500 rounded-lg p-0.5 btn hover:preset-tonal-primary">
        <div class='flex items-center gap-2 bg-white dark:bg-transparent rounded-md h-full p-2 px-3'>
          <Download class="h-4 w-4" />
          Resume
        </div>
      </button>
      <LightSwitch />
    </div>
    <div class='sm:hidden flex'>
      <button class="btn btn-icon btn-icon-lg hover:preset-tonal">
      <Menu class="h-6 w-6 text-foreground cursor-pointer" />
      </button>
    </div>
  {/snippet}
  <div class='hidden sm:flex items-center gap-4'>
    <a href="#about" class="transition-colors hover:text-foreground/80">
      About
    </a>
    <a href="#skills" class="transition-colors hover:text-foreground/80 ">
      Skills
    </a>
    <a href="#projects" class="transition-colors hover:text-foreground/80">
      Projects
    </a>
    <a href="#contact" class="transition-colors hover:text-foreground/80">
      Contact
    </a>
</div>
</AppBar>

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
