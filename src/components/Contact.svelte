<script>
	import { Github, Linkedin, Mail } from "@lucide/svelte";

</script>
<section id="contact" class="container py-24">
    <div class="max-w-2xl mx-auto space-y-8">
      <div class="text-center space-y-4">
        <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl">Get In Touch</h2>
        <p class="text-muted-foreground">
          Have a project in mind? Let's discuss how we can work together to bring your ideas to life.
        </p>
      </div>

      <div class="flex justify-center space-x-6">
        <div class="text-center">
          <Mail class="h-6 w-6 mx-auto mb-2 text-primary" />
          <p class="text-sm font-medium">Email</p>
          <p class="text-sm text-muted-foreground">rmdabs@gmail.com</p>
        </div>
        <div class="text-center">
          <Github class="h-6 w-6 mx-auto mb-2 text-primary" />
          <p class="text-sm font-medium">GitHub</p>
          <p class="text-sm text-muted-foreground">@imarcobot</p>
        </div>
        <div class="text-center">
          <Linkedin class="h-6 w-6 mx-auto mb-2 text-primary" />
          <p class="text-sm font-medium">LinkedIn</p>
          <p class="text-sm text-muted-foreground">imarcobot</p>
        </div>
      </div>
    </div>
  </section>