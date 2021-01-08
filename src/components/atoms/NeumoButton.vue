<template>
  <button
    :class="[neumo, 'px-6', 'py-2', 'rounded-lg']"
  ><slot></slot></button>
</template>

<script>
export default {
  props: {
    neumo: {
      type: String,
      required: true,
    }
  }
}
</script>

<style scoped>
</style>