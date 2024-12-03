<script lang="ts">
	import '../app.css'
	let { children } = $props()
</script>

<svelte:head>
  <title>session.community</title>
</svelte:head>
{@render children()}
