<script lang="ts">
	import { page } from '$app/stores'
	import { handleSession } from '@lucia-auth/sveltekit/client'
	import Footer from './footer.svelte'
	import Heading from './heading.svelte'

	import '@skeletonlabs/skeleton/styles/all.css'
	import '@skeletonlabs/skeleton/themes/theme-crimson.css'
	import '../app.postcss'

	handleSession(page)
</script>

<svelte:head>
	<title>Brad's super duper cool blog!!!!</title>
	<link rel="icon" href="https://fav.farm/🔥" />
</svelte:head>

<Heading />
<slot />
<Footer />
