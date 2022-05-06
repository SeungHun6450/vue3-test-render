<template>
  <li>{{ name }}?!</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped lang="scss">
// scoped: 유효한 범위가 현재 컴포넌트다
  h1{
    color: red !important;
  }
</style>