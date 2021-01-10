<template>
  <v-col cols="10" lg="4" xl="6">
    <h2 class="text-center mb-8"><span class="font-rubik">SHARE</span></h2>
    <v-row justify="space-around">
      <a
        :href="v.url"
        v-for="v in sns"
        :key="v.url"
        target="blank"
      >
        <neumo-button-fab
          size="3"
          class=""
        >test</neumo-button-fab>
      </a>
      <a :href="shareOnHatena" target="blank">
        <neumo-button-fab
          size="3"
          class=""
        ><span>B!</span></neumo-button-fab>
      </a>
    </v-row>
  </v-col>
</template>

<script>
import NeumoButtonFab from '../atoms/NeumoButtonFab.vue'
export default {
  components: {
    NeumoButtonFab,
  },
  data() {
    return {
      url: process.env.VUE_APP_URL,
    }
  },
  computed: {
    sns() {
      return [
        {
          icon: ['fab', 'twitter'],
          url: `https://twitter.com/intent/tweet?url=${this.url}`
          },
        {
          icon: ['fab', 'facebook'],
          url: `https://www.facebook.com/sharer/sharer.php?u=${this.url}`
          },
        {
          icon: ['fab', 'line'],
          url: `http://line.me/R/msg/text/?${this.text} ${this.url}"`
          },
      ]
    },
    shareOnHatena() {
      return `http://b.hatena.ne.jp/entry/${this.url}`
    }
  }
}
</script>

<style>

</style>