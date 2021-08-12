<template>
  <div>
    <div>Привет мир</div>
    <button @click='fetchSomething'>Load</button>
  </div>
</template>

<script>
export default {

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
