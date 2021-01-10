<template>
    <v-col id="abc" cols="11" lg="8" xl="6" class="pt-3">
      <v-row align="center" class="mb-0 mb-sm-n1 px-3">
        <toggle-buttons
          :lists="lists"
          :is-active = isActive
          label="label"
          @click.native="$emit('my-click', isActive)"
          @my-click="isActive = $event"
          class="mr-1"
        ></toggle-buttons>
        <counter v-if="true" :count="count">words</counter>
      </v-row>
      <neumo-textarea
        placeholder="テキストを入力"
        neumo="concave"
        v-model="text"
        @focus.native="$vuetify.goTo('#abc')"
        @input="$emit('update', text)"
      ></neumo-textarea>
    </v-col>
</template>

<script>
import NeumoTextarea from '../atoms/NeumoTextarea.vue';
import Counter from '../molecules/Counter.vue';
import ToggleButtons from '../molecules/ToggleButtons.vue';

export default {
  props: {
    count: {
      type: Number,
      required: true,
    }
  },
  components: {
    ToggleButtons,
    NeumoTextarea,
    Counter,
  },
  data() {
    return {
      isActive: '日本語',
      lists: [{label: '日本語'}, {label: '英語'}],
      text: "",
    }
  }
}
</script>

<style>

</style>