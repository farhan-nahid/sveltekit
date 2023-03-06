<script lang="ts">
	import { page } from '$app/stores';

	const { slug } = $page.params;

	const slugArr: string[] = slug.split('/');
</script>

{#if slugArr.length === 0}
	<h1>No params yet</h1>
{:else if slugArr.length === 1}
	<h1>Param is {slug[0]}</h1>
{:else if slugArr.length === 2}
	<h1>Param is {slug[0]} & {slug[1]}</h1>
{:else}
	<h1>Total param length {slugArr.length}</h1>
	<h4>Full Slug is {slugArr}</h4>
{/if}
