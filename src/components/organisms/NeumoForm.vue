<template>
  <div>
    <p>{{isActive}}</p>
    <toggle-buttons
      :lists="lists"
      :is-active = isActive
      label="label"
      @my-click="isActive = $event"
    ></toggle-buttons>
  </div>
</template>

<script>
import ToggleButtons from '../molecues/ToggleButtons.vue';

export default {
  components: {
    ToggleButtons
  },
  data() {
    return {
      isActive: '日本語',
      lists: [{label: '日本語'}, {label: '英語'}],
    }
  }
}
</script>

<style>

</style>