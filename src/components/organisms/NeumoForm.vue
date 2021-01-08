<template>
  <v-row justify="center">
    <v-col lg="6">
      <toggle-buttons
        :lists="lists"
        :is-active = isActive
        label="label"
        class="mb-2"
        @my-click="isActive = $event"
      ></toggle-buttons>

      <neumo-textarea
        neumo="concave"
      ></neumo-textarea>
    </v-col>
  </v-row>
</template>

<script>
import NeumoTextarea from '../atoms/NeumoTextarea.vue';
import ToggleButtons from '../molecues/ToggleButtons.vue';

export default {
  components: {
    ToggleButtons,
    NeumoTextarea
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