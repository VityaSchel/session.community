<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='session-bots-directory'
  title='Session Bots Directory'
  hue={120}
  image='/images/session-bots-directory.webp'
  links={[
    { href: 'https://bots.session.community', label: 'bots.session.community' },
    { href: 'https://sogs.hloth.dev/session-bots-directory?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='A place to discover bots created by Session messenger developers community.'
  stack='Remix (my first Remix project), @shadcn/ui; Fastify, Node.js; Redis'
>
  <ul class="list-disc">
    <li>Free and <a href="https://github.com/VityaSchel/session-bots-directory">opensource</a></li>
    <li>No personal info is collected for signups</li>
    <li>Adding new bot is as easy as writing a little info about it and verifying response from bot to make sure you're the real author of it — it can be done in less than 60 seconds</li>
    <li>All moderation is automatically done by GPT. It does not allow any illegal topics and any visitor can report any bot anytime with instant notification to me for additional review</li>
    <li>All bots are automatically checked for uptime using custom checker built on top of my free&amp;opensource <a href="#sessionjs">bot framework for Session</a></li>
  </ul>
</Section>