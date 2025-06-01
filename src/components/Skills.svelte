<script lang='ts'>
  const skills = [
    {
      category: 'Frontend',
      technologies: ['React', 'Next.js', 'TypeScript', 'Tailwind CSS', 'Svelte', 'SvelteKit']
    },
    {
      category: 'Backend',
      technologies: ['Node.js', 'Express', 'Django']
    },
    {
      category: 'Databases',
      technologies: ['PostgreSQL']
    },
    {
      category: 'DevOps',
      technologies: ['Cloudflare', 'AWS', 'GitHub Actions']
    }
  ];
</script>

<section id="skills" class="container py-24">
    <div class="space-y-12">
      <div class="text-center space-y-4">
        <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl">Skills & Technologies</h2>
        <p class="text-muted-foreground max-w-2xl mx-auto">
          Here are the technologies and tools I work with to bring ideas to life.
        </p>
      </div>

      <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-4">
        {#each skills as skill}
        <div class="card p-6 preset-outlined-primary-500 card-hover preset-tonal-surface space-y-4">
          <header>
            <h3 class='h3'>{skill.category}</h3>
          </header>
          <article class="space-y-2 space-x-2">
            {#each skill.technologies as technology}
            <button class='chip preset-outlined-surface-500'>{technology}</button>
            {/each}
          </article>
          </div>
        {/each}
        
      </div>
    </div>
  </section>