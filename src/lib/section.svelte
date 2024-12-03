<script lang='ts'>
  import ExternalIcon from "$lib/icones/ExternalIcon.svelte"

  let { title, children, description, image, links, stack }: {
    title: string
    children: import('svelte').Snippet
    description: string
    image: string
    stack: string
    links: { href: string, label: string }[]
  } = $props()
</script>

<section class="min-h-screen p-20 flex gap-20">
  <div class="flex flex-col gap-10 shrink-0 w-[400px]">
    <img src={image} alt="" class="w-full rounded-sm">
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
    <h1 class="text-8xl font-black mb-5">{title}</h1>
    <p class="text-lg max-w-[800px] mb-5">{description}</p>
    <div>{@render children?.()}</div>
  </div>
</section>