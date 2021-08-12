<template>
	<header class="header">
		<div class='header__left'>
      <NuxtLink class='brand' to='/'>
        <img src='/img/logo.svg' alt='Abito'>
      </NuxtLink>
      <nav>
        <ul>
          <li></li>
        </ul>
      </nav>
    </div>
    <div class='header__right'>
      <div>
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
      <div v-else>
        Скрыто
      </div>
      <br>
      <br>
      <AppButton @click='toggleButton'> Toggle button </AppButton>
      <br>
      <br>
      <AppButton @click='toggleButtonShow'> Toggle hide</AppButton>
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
    toggleButton () {
	    this.buttonDisabled = !this.buttonDisabled
    },
    toggleButtonShow () {
	    this.show = !this.show
    }
  }
}
</script>

<style lang="sass" scoped>
	.header
		font-size: 12px
</style>
