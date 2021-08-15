<template>
  <div class='product container'>
		<div class="product__left">
			<h2 class="t24 fw7 mb25">Рекомендации для вас</h2>
			<div class="product-box">
				<ProductItem imgSrc="/img/1.png" title="Двухсторонняя ветровка для мальчика" price="2 110" adres="Казань, р-н Ново-Савиновский" date="10 июля 11:39" />
			</div>
		</div>
		<div class="product__right">
			<h2 class="t18 fw7 mb25">Сервисы и услуги</h2>
		</div>
  </div>
</template>

<script>
import ProductItem from '~/components/uikit/ProductItem'
export default {
  name: 'Product',
	components: {
	  ProductItem
	},
  props: {
    title: {
      type: String,
      required: true
    }
		
  }
}
</script>

<style lang="scss" scoped>
	.product{
		margin-top: 45px;
		display: flex;
		justify-content: space-between;
		&__left{
			width: 852px;
		}
		&-box{
			display: grid;
			grid-template-columns: repeat(3, 1fr);
			gap: 0 15px;
		}
		&__right{
			width: 230px;
			padding-top: 10px;
		}
	}
</style>
