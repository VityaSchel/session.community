<script lang='ts'>
  let scrolled = $state(0)
</script>

<svelte:window bind:scrollY={scrolled} />
<div class="flex flex-col items-center justify-center text-center gap-4 h-100svh bg-[#121212] px-16 relative">
  <h1 class="text-3xl md:text-5xl font-bold">session.community</h1>
  <p>A collection of tools, websites and community creations directories from <a href='https://hloth.dev'>hloth.dev</a></p>
  <span class="absolute bottom-5 animate-bounce transition-opacity" style="opacity: {scrolled > 100 ? 0 : 1}">
    <span class="animate-pulse">
        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="32" viewBox="0 0 448 512" class="rotate-180"><path fill="currentColor" d="M128 40c0-22.1 17.9-40 40-40s40 17.9 40 40v148.2c8.5-7.6 19.7-12.2 32-12.2c20.6 0 38.2 13 45 31.2c8.8-9.3 21.2-15.2 35-15.2c25.3 0 46 19.5 47.9 44.3c8.5-7.7 19.8-12.3 32.1-12.3c26.5 0 48 21.5 48 48v112c0 70.7-57.3 128-128 128h-85.3c-5 0-9.9-.3-14.7-1c-55.3-5.6-106.2-34-140-79L8 336c-13.3-17.7-9.7-42.7 8-56s42.7-9.7 56 8l56 74.7zm112 264c0-8.8-7.2-16-16-16s-16 7.2-16 16v96c0 8.8 7.2 16 16 16s16-7.2 16-16zm48-16c-8.8 0-16 7.2-16 16v96c0 8.8 7.2 16 16 16s16-7.2 16-16v-96c0-8.8-7.2-16-16-16m80 16c0-8.8-7.2-16-16-16s-16 7.2-16 16v96c0 8.8 7.2 16 16 16s16-7.2 16-16z"/></svg>
    </span>
  </span>
</div>
