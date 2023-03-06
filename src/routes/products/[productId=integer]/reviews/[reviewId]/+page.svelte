<script lang="ts">
	import { page } from '$app/stores';

	type propsType = {
		productId: string;
		reviewId: string;
	};

	const { productId, reviewId } = $page.params;
</script>

<h1>
	Review {reviewId} for product {productId}
</h1>
