<script>
  import Hero from "$lib/hero.svelte"
  import OnsRegistry from "$lib/ons-registry.svelte"
  import SessionBotsDirectory from "$lib/session-bots-directory.svelte"
  import Bunsogs from "$lib/bunsogs.svelte"
  import SessionJs from "$lib/session-js.svelte"
  import SessionNative from "$lib/session-native.svelte"
  import SessionVanityId from "$lib/session-vanity-id.svelte"
  import WatchOsClient from "$lib/session-watchos-client.svelte"
  import SessionWebClient from "$lib/session-web.svelte"
</script>

<svelte:head>
  <title>session.community</title>
  <meta property="og:title" content="session.community" />
  <meta property="og:url" content="https://session.community/" />
</svelte:head>
<Hero />
<OnsRegistry />
<SessionBotsDirectory />
<Bunsogs />
<SessionJs />
<SessionNative />
<SessionVanityId />
<WatchOsClient />
<SessionWebClient />