<template>
  <div class='product'>
    {{title}}
  </div>
</template>

<script>
export default {
  name: 'Product',

  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
