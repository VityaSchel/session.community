<script lang='ts'>
  import ExternalIcon from "$lib/icones/ExternalIcon.svelte"

  let { id, title, hue = 0, saturation = 100, brightness = 4, children, description, image, links, stack }: {
    id: string
    title: string
    hue?: number
    saturation?: number
    brightness?: number
    children: import('svelte').Snippet
    description: string
    image: string
    stack: string
    links: { href: string, label: string }[]
  } = $props()
</script>

<a
  href="#{id}" 
  class="absolute opacity-0 pointer-events-none"
  id={id}
>
  Skip to «{title}»
</a>
<section
  class="min-h-100lvh p-10 lg:p-20 flex flex-col-reverse lg:flex-row gap-20 section-gradient"
  style='--bg: hsl({hue}deg, {saturation}%, {brightness}%)'
>
  <div class="flex flex-col gap-10 shrink-0 items-center w-full lg:w-[400px]">
    <img src={image} alt="" class="rounded-md w-[400px]">
    <span class="text-white/50 font-mono">{stack}</span>
    <div class="flex flex-col gap-3">
      {#each links as link (link.href)}
        <a href={link.href} class="text-xl font-medium flex items-center gap-1 w-fit no-underline">
          <span class="w-5 h-5 svg-full"><ExternalIcon /></span> {link.label}
        </a>
      {/each}
    </div>
  </div>
  <div class="flex flex-col gap-2">
    <h1 class="text-6xl md:text-7xl lg:text-8xl font-black mb-5">{title}</h1>
    <p class="text-lg max-w-[800px] mb-5">{description}</p>
    <div>{@render children?.()}</div>
  </div>
</section>

<style>
  .section-gradient {
    background: linear-gradient(135deg, var(--bg), black);
  }
</style>