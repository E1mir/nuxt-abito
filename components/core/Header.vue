<template>
	<header class="header container">
		<div class='header__left'>
      <NuxtLink class='brand' to='/'>
        <img src='/img/logo.svg' alt='Abito'>
      </NuxtLink>
      <nav>
        <ul class="nav t14">
          <li><a href="#">Авто</a></li>
					<li><a href="#">Недвижимость</a></li>
					<li><a href="#">Работа</a></li>
					<li><a href="#">Услуги</a></li>
        </ul>
      </nav>
    </div>
    <div class='header__right'>
      <div class="registration">
        Вход и регистрация
      </div>
      <AppButton
        v-if='show'
        type='white'
        :disabled='buttonDisabled'
        @click='onPostAnAd'
      >
        Подать объявление
      </AppButton>
    </div>
	</header>
</template>

<script>
import AppButton from '~/components/uikit/AppButton'
export default {
	name: 'Header',

  components: {
	  AppButton
	},

  data () {
	  return {
	    buttonDisabled: false,
      show: true
    }
  },

  methods: {
	  onPostAnAd () {
	    console.log('Open ad page')
    },
  }
}
</script>

<style lang="scss" scoped>
	@import "assets/scss/variables";
	.header{
		color: $color-text;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 30px 0;

		&__left, &__right{
			display: flex;
			align-items: center;
		}

	}

	.registration{
		margin-right: 25px;
	}

	.nav{
		display: flex;
		align-items: center;
		li{
			margin-right: 14px;
			display: inline-block;
		}
		a{
			text-decoration: none;
			color: $color-text;
			transition: all 0.4s;
			&:hover{
				color: $color-primary;
			}
		}
	}

	.brand{
		margin-right: 20px;
		width: 58px;
	}

</style>
