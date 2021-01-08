<template>
  <v-app>
    <custom-header></custom-header>
    <main-page></main-page>
  </v-app>
</template>

<script>
import MainPage from '@/components/pages/MainPage.vue';
import CustomHeader from './components/molecues/CustomHeader.vue';

export default {
  name: 'App',

  components: {
    MainPage,
    CustomHeader,
  },
};
</script>

<style>
  main, .header{
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
