<template>
	<main>
		<Header class='layout__header'/>
		<Search/>
		<Nuxt/>
	</main>
</template>

<script>
import Header from '@/components/core/Header.vue';
import Search from '@/components/core/Search.vue';

export default {
	components: {
		Header,
		Search
	}
}

</script>

<style lang='scss'>

</style>
