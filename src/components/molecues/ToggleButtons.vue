<template>
  <div>
    <neumo-button
      v-for="(list, index) in lists"
      :key="list[label]"
      :class="index != lists.length -1 ? 'mr-2' : '' "
      :neumo="activation(list[label])"
      @click.native="$emit('my-click', list[label])"
    >{{list[label]}}</neumo-button>
  </div>
</template>

<script>
import NeumoButton from '../atoms/NeumoButton.vue'
export default {
  props: {
    lists: {
      type: Array,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    isActive: {
      type: String,
      required: true,
    },
  },
  components: {
    NeumoButton,
  },
  computed: {
    activation() {
      return (state) => {
        return this.isActive == state ? 'concave' : 'convex'
      }
    }
  }
}
</script>

<style>

</style>