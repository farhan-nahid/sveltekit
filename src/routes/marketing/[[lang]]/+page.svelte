<script lang="ts">
	import { page } from '$app/stores';

	type langType = 'en' | 'es' | 'fr';

	type greetingsType = {
		en: string;
		es: string;
		fr: string;
	};

	const greetings: greetingsType = {
		en: 'Hello!',
		es: 'Hola!',
		fr: 'Bangjour!'
	};

	const lang: langType = ($page.params.lang as langType) ?? 'en';

	const word: string = greetings[lang];
</script>

<h1>Marketing Lang {word}</h1>
