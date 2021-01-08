<template>
  <v-app>
    <v-main>
      <div class="ma-10 pa-14">
        <neumo-form></neumo-form>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import NeumoForm from './components/organisms/NeumoForm.vue';

export default {
  name: 'App',

  components: {
    NeumoForm,
  },
};
</script>

<style>
  main {
    background-color: #F3F3F4 !important;
  }
  .convex {
    background: #F3F3F4 !important;
    box-shadow: -5px -5px 20px #FFFFFF, 5px 5px 20px rgba(189, 195, 197, 0.5);
  }

  .concave {
    box-shadow: inset -4px -2px 8px #FFFFFF, inset 4px 2px 8px rgba(189, 195, 197, 0.48);
  }
</style>
