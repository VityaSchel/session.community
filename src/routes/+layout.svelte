<script lang="ts">
	import '../app.css'
	let { children } = $props()
</script>

<svelte:head>
  <title>session.community</title>
  <meta name="description" content="A collection of tools, websites and community creations directories from hloth.dev">
  <link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
  <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
  <link rel="shortcut icon" href="/favicon.ico" />
  <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
  <link rel="manifest" href="/site.webmanifest" />
</svelte:head>
{@render children()}
