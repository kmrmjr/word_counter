<template>
  <textarea :class="[neumo, 'rounded-xl', 'px-4', 'py-6']" cols="30" rows="10"></textarea>
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

<style>
textarea {
  resize: none !important;
  outline: none;
  width: 100%;
}
</style>