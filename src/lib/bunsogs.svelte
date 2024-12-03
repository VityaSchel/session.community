<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='bunsogs'
  title='Bunsogs'
  saturation={5}
  brightness={15}
  image='/images/bunsogs.png'
  links={[
    { href: 'https://github.com/vityaSchel/bunsogs/', label: 'Bunsogs GitHub' },
    { href: 'https://sogs.hloth.dev/bunsogs?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Session Open Group Server implementation written in JavaScript using bun.sh.'
  stack='Bun, TypeScript'
>
  <p>Aims to be very fast, flexible and extensible. Drop-in replacement for pysogs — works with the same database schema. Bunsogs support everything pysogs has, but it's better.</p>
  <ul class="list-disc">
    <li>Plugins (antispam, anticsam, DM greetings)</li>
    <li>Bot API</li>
    <li>GUI CLI</li>
    <li>Per-room rate limit settings</li>
    <li>Per-room old messages pruning settings</li>
    <li>Only allow certain attachments (e.g. no images, only voice)</li>
    <li>Global permissions overrides</li>
  </ul>
  <br />
  <p>Can be used on any OS where Bun runs (any Linux, Windows, MacOS)</p>
</Section>