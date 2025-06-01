<script>
	import { Github, Linkedin, MapPin } from "@lucide/svelte";

</script>
<section class="container py-24 md:py-32">
    <div class="grid gap-8 lg:grid-cols-2 lg:gap-12 items-center">
      <div class="space-y-6">
        <div class="space-y-2">
          <h1 class="text-4xl font-bold tracking-tighter sm:text-5xl md:text-6xl">
            Rowmel Marco
            <span class="text-primary"> Dabon</span>
          </h1>
          <p class="text-xl text-muted-foreground max-w-[600px]">
            I make magic happen, one feature at a time.
          </p>
        </div>
        <div class="flex items-center space-x-2 text-sm text-muted-foreground">
          <MapPin class="h-4 w-4" />
          <span>Davao City, PH</span>
        </div>
        <div class="flex items-center space-x-4">
          <a href="https://github.com/rmudabon" class='btn-icon hover:preset-tonal' target="_blank" rel="noopener noreferrer">
            <Github class="h-5 w-5" />
          </a>
          <a class='btn-icon hover:preset-tonal' href='https://www.linkedin.com/in/rmudabon/' target="_blank" rel="noopener noreferrer">
            <Linkedin class="h-5 w-5" />
          </a>
        </div>
      </div>
    </div>
  </section>