<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='id-session-community'
  title='id.session.community'
  hue={120}
  image='/images/id-session-community.webp'
  links={[
    { href: 'https://id.session.community', label: 'id.session.community' },
    { href: 'https://github.com/VityaSchel/id.session.community', label: 'Website on GitHub' },
    { href: 'https://github.com/VityaSchel/cf-ons-resolver', label: 'API source' }
  ]}
  description='A static client-side web site that allows anyone to create a link to their Session ID and invite others to chat with them on Session'
  stack='Svelte, SvelteKit, Tailwind CSS, Cloudflare Workers'
>
  <ul class="list-disc">
    <li>Free and <a href="https://github.com/VityaSchel/id.session.community">opensource</a></li>
    <li>Visits are not logged thanks to URL fragment hash-based routing</li>
    <li>Automatic ONS resolving built on top of Cloudflare Workers and Edge Elysia</li>
  </ul>
</Section>