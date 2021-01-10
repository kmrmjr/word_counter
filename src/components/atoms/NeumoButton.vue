<template>
  <button
    :class="[neumo, 'px-6', 'py-2', 'rounded-lg', 'font-weight-bold', 'grey--text', 'text--darken-3']"
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