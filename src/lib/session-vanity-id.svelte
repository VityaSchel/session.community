<script lang='ts'>
  import Section from "./section.svelte"
</script>

<Section
  id='session-vanity-id'
  title='Session Vanity ID'
  hue={270}
  image='/images/session-vanity-id.png'
  links={[
    { href: 'https://session-id.pages.dev', label: 'Generator website' },
    { href: 'https://github.com/VityaSchel/session-id-generator', label: 'GitHub sources & faster CLI' },
    { href: 'https://sogs.hloth.dev/session-vanity-id-generator?public_key=8948f2d9046a40e7dbc0a4fd7c29d8a4fe97df1fa69e64f0ab6fc317afb9c945', label: 'Announcements SOGS' }
  ]}
  description='Simple, fast and flexible Session ID vanity generator tool.'
  stack='Bun, TypeScript'
>
  <p>This tool bruteforces mnemonics and looks for Session IDs matching your specific pattern. The website works 100% clientside and allows you to specify how many workers you want to spawn.</p>
  <p>I recommend inputting 4 to 5 characters if you have a decent PC.</p>
  <p>You can configure how many workers to spawn (from 1 to Math.ceil(navigator.hardwareConcurrency / 3)) and that directly influences how many IDs per second your PC will bruteforce. But most likely your PC will limit threads to about 60%-80% of maximum allowed threads to spawn. Basically, setting 10 workers will likely get you same results as settings 7 workers.</p>
  <p>Number of characters you inputted DOES NOT practically affect bruteforce speed. So type anything, look at "XXXX IDs/s" and compare that number to this table (I take 30k ids/s as average):</p>
  <table>
    <thead>
      <tr><th>Characters after "05"</th><th>Time for 50% probability (seconds)</th><th>Time for 25% probability (seconds)</th></tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>0.00036</td><td>0.00015</td></tr>
      <tr><td>2</td><td>0.0059</td><td>0.0025</td></tr>
      <tr><td>3</td><td>0.0946</td><td>0.0393</td></tr>
      <tr><td>4</td><td>1.5142</td><td>0.6284</td></tr>
      <tr><td>5</td><td>24.227</td><td>10.055</td></tr>
      <tr><td>6</td><td>387.636</td><td>160.883</td></tr>
      <tr><td>7</td><td>6202 (1.7 hours)</td><td>2574</td></tr>
      <tr><td>8</td><td>99234 (27 hours)</td><td>41186</td></tr>
      <tr><td>9</td><td>1587757 (18 days)</td><td>658978</td></tr>
      <tr><td>10</td><td>25404112 (294 days)</td><td>10543659</td></tr>
    </tbody>
  </table>
</Section>