<template>
  <button
    class='app-button'
    :class='{
    "app-button--default": buttonType === "default",
    "app-button--white": buttonType === "white",
    "app-button--text": buttonType === "text"
  }'
  :disabled='disabled'
  @click='onClick'
  >
    <slot/>
  </button>
</template>

<script>

export default {
  name: 'AppButton',

  props: {
    buttonType: {
      type: String,
      default: 'default'
    },
    disabled: {
      type: Boolean,
      default: false
    }
  },


  methods: {
    onClick () {
      if (!this.disabled) {
        this.$emit('click')
      }
    }
  }
}
</script>

<style lang='scss' scoped>
@import "assets/scss/variables";

.app-button {
  padding: 10px 15px;
  font-size: 14px;
  border-radius: 5px;
  transition: 0.3s all;
  cursor: pointer;
  border: 1px solid transparent;
  background: none;
  color: white;

  &--default {
    background-color: $color-primary;
    color: white;

    &:hover {
      background-color: $color-primary-hover;
    }
  }

  &--white {
    background-color: white;
    color: $color-primary;
    border-color: $color-primary;

    &:hover {
      background-color: $color-primary-hover;
      color: white;
    }
  }

  &[disabled] {
    cursor: not-allowed;
    background-color: #c4c4c4;
    color: white;
  }
}
</style>
