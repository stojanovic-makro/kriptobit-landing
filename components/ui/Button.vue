<template>
  <div class="button" :class="color" :style="{ height: height }">
    <div class="row" style="align-items: center; justify-content: center; padding-top: 2px">
      <div>{{ label }}</div>
      <img style="padding-bottom: 3px; margin-left: 12px" src="/icons/arrow_right.svg">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    label: {
      type: String,
      default: 'Click'
    },
    height: {
      type: String,
      default: 'auto'
    },
    color: {
      type: String,
      default: 'bg-white'
    }
  }
}
</script>