<script lang="ts">
	import { Moon, Sun } from '@lucide/svelte';

  let checked = $state(false);

  $effect(() => {
    const mode = localStorage.getItem('mode') || 'light';
    checked = mode === 'dark';
  });

  const onCheckedChange = (isChecked: boolean) => {
    const mode = isChecked ? 'dark' : 'light';
    document.documentElement.setAttribute('data-mode', mode);
    localStorage.setItem('mode', mode);
    checked = isChecked;
  };

</script>

<svelte:head>
  <script>
    const mode = localStorage.getItem('mode') || 'light';
    document.documentElement.setAttribute('data-mode', mode);
  </script>
</svelte:head>

<label for='dark-mode' class="btn-icon hover:preset-tonal btn-icon-lg cursor-pointer">
  {#if checked}
    <Moon class="w-6" />
  {:else}
    <Sun class="w-6" />
  {/if}
</label>
<input type="checkbox" id="dark-mode" class='hidden' onclick={(event) => {
  onCheckedChange(event.currentTarget.checked)
}} {checked}>