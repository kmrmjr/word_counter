<template>
  <v-app>
    <custom-header></custom-header>
    <main-page></main-page>
  </v-app>
</template>

<script>
import MainPage from '@/components/pages/MainPage.vue';
import CustomHeader from './components/molecules/CustomHeader.vue';

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
    background-color: #e7e7e7 !important;
  }
  .convex {
    background: #e7e7e7 !important;
    box-shadow: -5px -2px 5px #FFFFFF, 5px 2px 5px rgba(118, 122, 122, 0.5);
  }

  .concave, .convex:active {
    box-shadow: inset -4px -2px 8px #FFFFFF, inset 4px 2px 8px rgba(118, 122, 122, 0.5);
  }

  *:focus {
    outline: none;
  }
</style>
