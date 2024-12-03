<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='session-native'
  title='Session Native'
  hue={50}
  image='/images/session-native.png'
  links={[
    { href: 'https://github.com/VityaSchel/session-native', label: 'Session Native GitHub' },
    { href: 'https://sogs.hloth.dev/session-native?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Opensource Session client written with performance, design and user experience in mind.'
  stack='Swift, C++, SwiftData, Bun'
>
  <p>Uses native Swift and other native technologies of macOS and aims to run with latest technologies rather to be compatible with all devices, thus it requires at least macOS 14.0 or later.</p>
  <p>Isn't entirely native, as its backend is written with my <a href='#sessionjs'>Session.js</a> crossplatform Session framework. It doesn't matter though, because frontend must be reactive and backend can be anything. You won't experience any lags, because data is stored/retrieved using native SwiftData. Moreover, Session.js is written in Bun, which is very fast and comparable to Rust or even low-level languages.</p>
  <p>No onion routing for now, but you can setup onion routing on your network side yourself, also proxy settings are available</p>
  <p>While macOS protects applications data good enough, please be aware that app database is not encrypted, and thus can be accessed if malware has unrestricted access to your filesystem and you allowed it to read apps storage. Mnemonics are stored in keychain, which should make their retrieval harder for malicious actors.</p>
</Section>