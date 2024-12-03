<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='session-watchos-client'
  title='Apple Watch client'
  hue={290}
  image='/images/session-watchos.png'
  links={[
    { href: 'https://github.com/VityaSchel/session-watchos', label: 'GitHub source' },
    { href: 'https://sogs.hloth.dev/session-watchos?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Unofficial Session messenger client for Apple Watch, targeting watch OS 10.'
  stack='C, Swift'
>
  <p>Supported features:</p>
  <ul class="list-disc">
    <li>Send & receive messages</li>
    <li>ONS resolving</li>
  </ul>
  <br />
  <p>Signing in requires a server with hosted companion website. In simple terms, user is redirected there to input their mnemonic on any device they find comfortable and secure. Mnemonic is encrypted locally and stored on server shortly for watches to sync into its storage. Read in details in website's repository.</p>
</Section>