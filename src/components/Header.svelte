<script>
	import { Download, Menu } from "@lucide/svelte";
	import { AppBar, Modal } from "@skeletonlabs/skeleton-svelte";
	import LightSwitch from "./LightSwitch.svelte";

    let drawerState = $state(false)

    const drawerClose = () => {
        drawerState = false
    }

</script>
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
      <Modal
        open={drawerState}
        onOpenChange={(e) => (drawerState = e.open)}
        triggerBase="btn btn-icon btn-icon-lg hover:preset-tonal sm:hidden flex"
        contentBase="bg-surface-100-900 p-4 space-y-4 shadow-xl w-[480px] h-screen"
        positionerJustify="justify-start"
        positionerAlign=""
        positionerPadding=""
        transitionsPositionerIn={{ x: -480, duration: 200 }}
        transitionsPositionerOut={{ x: -480, duration: 200 }}
        >
        {#snippet trigger()}
            <Menu class="h-6 w-6 text-foreground cursor-pointer" />
        {/snippet}
        {#snippet content()}
            <div class="flex flex-col gap-4">
                <a href="#about" class="transition-colors hover:text-foreground/80" onclick={drawerClose}>
                    About
                  </a>
                  <a href="#skills" class="transition-colors hover:text-foreground/80" onclick={drawerClose}>
                    Skills
                  </a>
                  <a href="#projects" class="transition-colors hover:text-foreground/80" onclick={drawerClose}>
                    Projects
                  </a>
                  <a href="#contact" class="transition-colors hover:text-foreground/80" onclick={drawerClose}>
                    Contact
                  </a>
                </div>
        {/snippet}
    </Modal>
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