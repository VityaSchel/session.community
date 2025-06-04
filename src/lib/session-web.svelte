<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='session-web'
  title='Session Web'
  hue={20}
  image='/images/session-web.webp'
  links={[
    { href: 'https://session-web.pages.dev', label: 'Session in Web browser' },
    { href: 'https://github.com/VityaSchel/session-web', label: 'GitHub source' },
    { href: 'https://sogs.hloth.dev/session-watchos?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Experimental project running Session messenger in a web browser online.'
  stack='Bun, Vite'
>
  <p>Works in Tor! 99% client-side (still requires proxy to swarms though). All encryption and private keys never leave browser.</p>
  <ul class="list-disc">
    <li>Sending messages (no attachments support)</li>
    <li>Receiving messages</li>
    <li>Multiaccount</li>
    <li>Localization in 2 languages</li>
  </ul>
  <br />
  <p>Be aware that I didn't care about best practices when writing this code, it does not use any security measures implemented in official clients, it does not prevent you from any kind of malicious attack, for example MITM. Backend requests to nodes aren't onion routed. SSL certificate pinning is not implemented (bun does not support this yet). This client does not support any cool features and is not maintained for security vulnerabilities found in code or dependencies.</p>
</Section>