<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='lokinet-vanity-address'
  title='Lokinet Vanity address generator'
  hue={200}
  image='/images/lokinet-vanity-address.webp'
  links={[
    { href: 'https://github.com/VityaSchel/lokinet-vanity-address-generator', label: 'GitHub sources & releases' }
  ]}
  description='This tool generates vanity lokinet onion router addresses for darknet websites using bruteforce math.'
  stack='Bun, TypeScript'
>
  <p>I have developed it by reading sources of the lokinet router itself written in C++</p>
  <p>Based on lokinet's ServiceInfo and Identity. Proto version can be found here (as of 8th March 2025, it's 0).</p>
  <p>Lokinet address is: <code>zbase32(signingKey) + ".loki"</code>, where signingKey (32 bytes) is <code>crypto_scalarmult_ed25519_base_noclamp(clamp_for_curve25519(sha512(random_seed)))</code></p>
  <p>.private file is <code>bencode(&#123; &quot;s&quot;: sValue, "v": 0 &#125;)</code> where sValue (64 bytes) is concatenated seed used to derive signingKey (32 bytes) and signingKey (32 bytes)</p>
</Section>