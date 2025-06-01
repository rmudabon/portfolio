<script lang="ts">
	import { AppBar } from '@skeletonlabs/skeleton-svelte';
	import '../app.css';
	import LightSwitch from '../components/LightSwitch.svelte';
	import { Code, Download } from '@lucide/svelte';

	let { children } = $props();
</script>

<style>
  .dotted { 
    background-image: radial-gradient(circle at 1px 1px, rgb(170, 170, 170) 1px, transparent 0);
    background-size: 65px 65px;
  }
</style>

<div>
<AppBar classes='bg-transparent/95 sticky top-0 z-50 backdrop-blur' headlineClasses="sm:hidden" centerClasses="flex justify-center items-center gap-4">
  {#snippet lead()}
  <a href="/" class="btn">
    <Code class="h-6 w-6" />
    <span class="font-bold text-xl">Marco Dabon</span>
  </a>
  {/snippet}
  {#snippet trail()}
    <button class="bg-linear-to-bl from-violet-500 to-fuchsia-500 rounded-lg p-0.5 btn hover:preset-tonal-primary">
      <div class='flex items-center gap-2 bg-white dark:bg-transparent rounded-md h-full p-2 px-3'>
        <Download class="h-4 w-4" />
        Resume
      </div>
    </button>
    <LightSwitch />
  {/snippet}
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
</AppBar>

<div class='dotted'>
  <div class="container mx-auto">
  {@render children()}
  </div>
</div>

<footer class="bg-muted/50">
  <div class="container py-8 mx-auto">
    <div class="flex flex-col sm:flex-row justify-between items-center space-y-4 sm:space-y-0">
      <div class="flex items-center space-x-2">
        <Code class="h-5 w-5" />
        <span class="font-semibold">Marco Dabon</span>
      </div>
      <p class="text-sm text-muted-foreground">© 2024 Marco Dabon. All rights reserved.</p>
    </div>
  </div>
</footer>
</div>
