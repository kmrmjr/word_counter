<template>
  <button
  :class="[
    'rounded-circle',
    'convex',
    `size-${size}`,
    'font-weight-bold',
    'grey--text',
    'text--darken-2']"   
  ><slot></slot></button>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      requred: true,
    },
  }
}
</script>

<style lang="scss">

  @mixin square($len) {
    width: $len;
    height: $len;
    }

  .size {
    &-1 {
      @include square(40px)
    }
    &-2 {
      @include square(50px)
    }
    &-3 {
      @include square(60px)
    }
  }

</style>