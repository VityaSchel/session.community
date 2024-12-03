<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='ons-registry'
  title='ONS Registry'
  hue={225}
  image='/images/ons-registry.png'
  links={[
    { href: 'https://ons.session.community', label: 'ons.session.community' },
    { href: 'https://sogs.hloth.dev/ons-registry?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Open OXEN Name System list, updated automatically from the blockchain.'
  stack='React, Next.js, next-pwa'
>
  <p>Explore ONS records in OXEN blockchain, filter by owner, lookup by partial text query for unhashed names, view estimated money spent on all records by specified owner. Local-first, fully mobile-optimized. Purchase system allows you to buy any ONS name in 30 seconds without having to own oxen wallet and buying crypto — just type in name you want, pay money and it will be automatically pushed to blockchain along with sending you wallet-owner mnemonic to specified email (if you specified it).</p>
  <ul class="list-disc">
    <li>Service Worker
      <ul class="list-[circle]">
        <li>Caches all assets for offline visits</li>
        <li>Downloads whole ONS db (2mb) if user is connected to Wi-Fi, has "saveData" set to false in device settings and has fast connection speed. Then uses this database when user visits ONS Registry being offline. Updates are based on E-Tag header.</li>
        <li>Otherwise, falls back to remote searches. In any case, any new found hash matches are cached to server using Background Sync web interface</li>
      </ul>
    </li>
    <li>For hashing and encryption, I'm using WebAssembly on frontend and crypto module in Node.js on backend</li>
    <li>For storage I'm using Cache API web interface on frontend and sqlite on backend</li>
    <li>Fully localized for two languages using next-i18next</li>
    <li>Integrated with YooKassa API for payments and shell for communication with oxen daemon.</li>
    <li>Automatically fetches, parses and analyzes new blockchain transactions via JsonRPC api connected to public node</li>
    <li>Uses CoinGecko API and OXEN coin historical price data to estimate how much money owner spent on their records</li>
    <li>Uses custom Monero base58 encoding to convert between ed25519 keypairs and OXEN wallet addresses</li>
    <li>Accessibility and fancy design built with @shadcn/ui</li>
    <li>No ads and bullshit. Free API for everyone with <a href="https://gist.github.com/VityaSchel/72210ebeb247816d09261b5194159cc6" rel="nofollow">API docs</a></li>
  </ul>
</Section>