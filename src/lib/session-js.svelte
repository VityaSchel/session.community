<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='sessionjs'
  title='Session.js'
  hue={80}
  image='/images/session-js.webp'
  links={[
    { href: 'https://sessionjs.github.io/docs/', label: 'Documentation' },
    { href: 'https://sogs.hloth.dev/sessionjs?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='JavaScript library for programmatic use of the Session messenger'
  stack='Bun, TypeScript, SQLite'
>
  <p>Supports server and browser environment with built-in proxy network module. Shipped with TypeScript definitions. Tested with bun:test. Written with blazingly fast Bun</p>
  <p>Session.js allows you to create:</p>
  <ul class="list-disc">
    <li>Highly optimized Session bots (hundreds of bots in a single app)</li>
    <li>Custom Session clients (web-based and native with JS backend)</li>
    <li>Automation tools for Session</li>
  </ul>
  <br />
  <p>Features:</p>
  <ul class="list-disc">
    <li>On-demand polling — you decide when to get new messages and whether instance should poll them (and poll settings like frequency) or work just for sending</li>
    <li>Per-instance storage and network settings — you can attach persistant storage to instance or use in-memory storage for throwaway one-time instances</li>
    <li>Session.js can be used in browser, keeping private keys on client-side and doing network requests on server-side. See this in action with my <a href='#session-web'>full-featured Session Web client!</a></li>
  </ul>
</Section>