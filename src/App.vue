<template>
  <v-app dark class="black" id="app">
    <v-flex class="pa-5" style="font-size: 2em; position: absolute; top: 0; left: 0; z-index: 999;">
      <h1>Something</h1>
    </v-flex>

    <v-layout column id="info" class="height" style="background: -webkit-linear-gradient(to right, #232526, #414345); z-index: 0;">
      <span class="hidden-sm-and-down my-auto mx-auto" style="font-size: 3em; text-shadow: 0 0 1em white">Fullstack
        <h1 style="z-index: 1">Web Developer</h1>
      </span>
      <h1 style="z-index: 1; font-size: 2em;  text-shadow: 0 0 1em white; text-align: center;" class="hidden-md-and-up my-auto mx-auto">Fullstack Web Developer</h1>
    </v-layout>

  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      //
    }
  }
}
</script>

<style media="screen">
  @import url('https://fonts.googleapis.com/css?family=Montserrat:900');
  * {
    font-family: 'Montserrat'; color: #444;
  }
  ::-webkit-scrollbar{
    width: 0;
  }
  .height {
    height: 100vh;
  }
  .round1 {
    border-radius: 1em;
  }
  .round2 {
    border-radius: 2em;
  }
</style>
