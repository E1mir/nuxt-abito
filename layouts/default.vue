<template>
	<main>
		<Header class='layout__header'/>
		<Nuxt/>
	</main>
</template>

<script>
import Header from '@/components/core/Header.vue';

export default {
	components: {
		Header
	}
}

</script>

<style lang='scss'>
.layout {
  &__header {
    .header__left {
      font-size: 25px;
    }
  }
}
</style>
