<script lang="ts">
	import { afterNavigate, beforeNavigate, goto } from '$app/navigation';

	const handelClick = () => {
		// goto('/products', { replaceState: true });
		goto('/');
	};

	beforeNavigate((navigation) => console.log({ before: navigation }));
	afterNavigate((navigation) => console.log({ after: navigation }));
</script>

<h1>Products</h1>

<button on:click={handelClick}>Home</button>
