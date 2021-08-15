<template>
  <NuxtLink to="/" class='product-item'>
    <div class="product-item__img mb10">
			<img :src="imgSrc" alt="">
		</div>
		<div class="product-item__title mb5">
			<div class="t16 fw7 trg">
				{{title}}
			</div>

			<div class="like">
				<img src="/img/like.svg" alt="like">
			</div>
		</div>
		<div class="t16 fw7 mb10">
			{{price}} ₽
		</div>
		<div class="t14 gray">
			{{adres}}
		</div>
		<div class="t14 gray">
			{{date}}
		</div>
  </NuxtLink>
</template>

<script>
export default {
  name: 'ProductItem',
	
  props: {
    imgSrc: {
      type: String,
    },
		title: {
      type: String,
      // required: true
    },
		price: {
      type: String,
      // required: true
    },
		adres: {
      type: String,
      // required: true
    },
		date: {
      type: String,
      // required: true
    },

  }
}
</script>

<style lang="scss" scoped>
	@import "assets/scss/variables";
	.product-item{
		text-decoration: none;
		color: $color-text;
		&__img{
			height: 178px;
			border-radius: 10px;
			overflow: hidden;
			img{
				width: 100%;
				height: 100%;
				transition: all 1.4s;
			}
		}
		&:hover &__img img{
			transform: scale(1.5);
		}
		&__title{
			display: flex;
			justify-content: space-between;
		}
	}
	.like{
		width: 15px;
		flex-shrink: 0;
	}
</style>
