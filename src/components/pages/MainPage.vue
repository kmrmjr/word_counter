<template>
  <v-main>
    <v-container class="pt-14">
      <v-row justify="center" class="pb-10">
        <neumo-form
          :count="count"
          @my-click="language = $event"
          @update="text = $event"
        ></neumo-form>
      </v-row>
      <v-row justify="center">
        <share-on-sns></share-on-sns>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
import NeumoForm from '../organisms/NeumoForm.vue';
import ShareOnSns from '../organisms/ShareOnSns.vue';
export default {
  components: {
    NeumoForm,
    ShareOnSns,
  },
  data() {
    return {
      text: "",
      language: "日本語",
    }
  },
  computed: {
    count() {
      if(this.language == '日本語') {
        const textNoSpace = this.text.replace(/\s+/g, "");
        return textNoSpace.length
      }
      const textTrim = this.text.trim();
      if(textTrim == "") {
        return 0 
      }
      const words = textTrim.split(/\s+/g)
      return words.length
    }
  }
}
</script>

<style>

</style>
