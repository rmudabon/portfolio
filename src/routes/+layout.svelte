<script lang="ts">
	import { AppBar } from '@skeletonlabs/skeleton-svelte';
	import ArrowLeft from '@lucide/svelte/icons/arrow-left';
  	import Menu from '@lucide/svelte/icons/menu';
	import '../app.css';
	import LightSwitch from '../components/LightSwitch.svelte';

	let { children } = $props();
</script>

<div class="max-w-6xl mx-auto p-4 h-full">
<AppBar classes='bg-transparent' headlineClasses="sm:hidden" centerClasses="hidden sm:block">
  {#snippet lead()}
  <a href="/" class="btn">
    <ArrowLeft size={24} />
</a>
  {/snippet}
  {#snippet trail()}
    <div class="hidden space-x-4 sm:flex">
      <a href="/about" class="btn hover:preset-tonal-primary">About</a>
	  <LightSwitch />
    </div>
    <div class="block sm:hidden">
      <Menu size={20} />
    </div>
  {/snippet}
</AppBar>

{@render children()}
</div>
