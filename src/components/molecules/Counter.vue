<template>
  <v-col class="font-weight-bold grey--text text--darken-4">
    <p class="text-h5 text-sm-h4 mb-0"><span class="font-rubik">{{count}}</span></p>
    <p class="text-body text-sm-h6 mb-0"><span class="font-rubik"><slot></slot></span></p>
  </v-col>
</template>

<script>
export default {
  props: {
    count: {
      type: Number,
      required: true,
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Rubik&display=swap');
  
  .font-rubik {
    font-family: 'Rubik', sans-serif !important;
  }
  p {
    display: inline-block;
  }
</style>