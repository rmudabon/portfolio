<script lang='ts'>
    import { ArrowRight, Github, Linkedin, Mail, MapPin } from "@lucide/svelte";
</script>

<div class="min-h-screen bg-background">
    <section class="container py-24 md:py-32">
      <div class="grid gap-8 lg:grid-cols-2 lg:gap-12 items-center">
        <div class="space-y-6">
          <div class="space-y-2">
            <h1 class="text-4xl font-bold tracking-tighter sm:text-5xl md:text-6xl">
              Full-Stack
              <span class="text-primary"> Developer</span>
            </h1>
            <p class="text-xl text-muted-foreground max-w-[600px]">
              I make magic happen, one feature at a time.
            </p>
          </div>
          <div class="flex items-center space-x-2 text-sm text-muted-foreground">
            <MapPin class="h-4 w-4" />
            <span>Davao City, PH</span>
          </div>
          <div class="flex flex-col sm:flex-row gap-4">
            <button class="btn btn-lg preset-filled w-fit">
              Projects
              <ArrowRight class="ml-2 h-4 w-4" />
            </button>
          </div>
          <div class="flex items-center space-x-4">
            <button class='btn'>
              <Github class="h-5 w-5" />
            </button>
            <button class='btn'>
              <Linkedin class="h-5 w-5" />
            </button>
            <button class='btn'>
              <Mail class="h-5 w-5" />
            </button>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="container py-24 bg-muted/50">
      <div class="max-w-3xl mx-auto text-center space-y-6">
        <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl">About Me</h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          With over 3 years of experience in software development, I specialize in building modern web applications
          using React, Node.js, and cloud technologies. I'm passionate about writing clean, maintainable code and
          creating user experiences that delight and engage.
        </p>
        <p class="text-muted-foreground leading-relaxed italic text-sm">
          When I'm not coding, you can find me catching up to the latest technologies, creating side projects, or enjoying the world of video games!
        </p>
      </div>
    </section>

    <section id="skills" class="container py-24">
      <div class="space-y-12">
        <div class="text-center space-y-4">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl">Skills & Technologies</h2>
          <p class="text-muted-foreground max-w-2xl mx-auto">
            Here are the technologies and tools I work with to bring ideas to life.
          </p>
        </div>

        <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-4">
          <div class="card p-6 preset-outlined-primary-500 card-hover  space-y-4">
            <header>
              <h3 class='h3'>Frontend</h3>
            </header>
            <article class="space-y-2">
              <button class='chip preset-outlined-surface-500'>React</button>
              <button class='chip preset-outlined-surface-500'>Next.js</button>
              <button class='chip preset-outlined-surface-500'>TypeScript</button>
              <button class='chip preset-outlined-surface-500'>Tailwind CSS</button>
              <button class='chip preset-outlined-surface-500'>Vue.js</button>
            </article>
            </div>
        </div>
      </div>
    </section>

    <section id="projects" class="container py-24 bg-muted/50">
      <div class="space-y-12">
        <div class="text-center space-y-4">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl">Featured Projects</h2>
          <p class="text-muted-foreground max-w-2xl mx-auto">
            A selection of projects that showcase my skills and passion for development.
          </p>
        </div>

        <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
          <div class="card p-8 card-hover preset-outlined-primary-500">
            Coming soon...
          </div>
        </div>

        <div class="text-center">
          <button class="btn preset-outlined-primary-500">
            View All Projects
            <ArrowRight class="ml-2 h-4 w-4" />
          </button>
        </div>
      </div>
    </section>

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

    
  </div>


