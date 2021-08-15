<template>
	<div class="container">
		<div class="search">
			<input type="text" class="input search-input t14" name="search" placeholder="Поиск по объявлениям">
			<AppButton class="search-btn"
				:buttonImg="true" imgSrc="/img/search.svg"
      >
        Найти
      </AppButton>
		</div>
	</div>
</template>

<script>
import AppButton from '~/components/uikit/AppButton'
export default {
		name: 'Search',
		components: {
			AppButton
		},
}
</script>

<style lang="scss" scoped>
	@import "assets/scss/variables";
	.search{
		display: flex;
		justify-content: space-between;
		background: $color-primary;
		border-radius: 5px;
		&-input{
			width: 1036px;
			margin: 3px;
			
		}
		&-btn{
			// width: 66px;
			display: flex;
			align-items: center;
		}
	}

</style>