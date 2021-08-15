<template>
  <div>

    <Product title='Самокат'/>
  </div>
</template>

<script>
import Product from '~/components/product/Product'
export default {
  components: { Product },
  methods: {
    fetchSomething() {
      this.$nextTick(() => {
        this.$nuxt.$loading.start()
        setTimeout(() => this.$nuxt.$loading.finish(), 500)
      })
    }
  }
}
</script>
