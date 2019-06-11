<template>
  <v-app dark class="black">
    <div column class="absolute height width" style="background: url('https://images.unsplash.com/photo-1471175745768-f10817cdb901?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80') 50% 50% no-repeat; background-size: cover ; filter: blur(3px) brightness(70%);"></div>

    <!-- <span class="absolute pl-3" style="font-size: 4em !important; font-family: 'Faster One'"><span style="font-family: 'Monoton'">Some</span>thing</span> -->

    <v-layout column class="absolute center-abs" style="padding-top: 64px;">
      <v-layout column class="absolute width controls">
        <v-layout column class="width absolute">
          <div class="pa-2 hidden-xs-only" style="margin-top: calc(50vh - 44px);">0:00 / 1:59</div>
          <div class="pa-2 hidden-sm-and-up" style="margin-top: calc(90vw - 44px);">0:00 / 1:59</div>
          <v-progress-linear indeterminate color="white" class="ma-0"></v-progress-linear>
        </v-layout>
        <v-layout class="absolute center">
          <v-btn flat class="my-auto" icon><v-icon>skip_previous</v-icon></v-btn>
          <v-spacer></v-spacer>
          <v-btn flat class="my-auto" fab @click="play = !play" ><v-icon large>{{ play ? 'play_arrow' : 'pause' }}</v-icon></v-btn>
          <v-spacer></v-spacer>
          <v-btn flat class="my-auto" icon><v-icon>skip_next</v-icon></v-btn>
        </v-layout>
      </v-layout>
      <span class="absolute hidden-xs-only" style="font-size: 1.5em; text-orientation: upright;writing-mode: vertical-rl; width: 0; writing-mode: vertical-rl;left: 0;">JinSang</span>
      <span class="absolute hidden-xs-only" style="font-size: 1.5em; text-orientation: upright;writing-mode: vertical-rl; width: 0; margin-left: calc(50vh + 1em); top: 50vh; transform: translateY(-50%); right: -1.5em">life.</span>
      <v-flex class="cover hidden-xs-only" style="height: 50vh; width: 50vh; background: url('https://f4.bcbits.com/img/a4112783792_10.jpg') 50% 50% no-repeat; background-size: cover;">
        <audio autoplay>
          <source src="../public/herewego.mp3" type="audio/mpeg">
        </audio>
      </v-flex>
      <v-flex class="cover hidden-sm-and-up" style="height: 90vw; width: 90vw; background: url('https://f4.bcbits.com/img/a4112783792_10.jpg') 50% 50% no-repeat; background-size: cover;">
        <audio autoplay>
          <source src="../public/herewego.mp3" type="audio/mpeg">
        </audio>
      </v-flex>
      <v-layout row class="my-2">
        <h1 class="hidden-xs-only">herewego</h1>
        <v-layout column class="hidden-sm-and-up">
          <span>herewego</span>
          <span class="grey--text">Jinsang</span>
        </v-layout>
        <v-spacer></v-spacer>
        <v-btn flat icon @click="loop = !loop" :color="loop ? 'amber lighten-2' : 'white' "><v-icon>{{ loop ? 'repeat_one' : 'repeat' }}</v-icon></v-btn>
        <v-btn flat icon @click="shuffle = !shuffle" :color="shuffle ? 'green lighten-2' : 'white' "><v-icon>shuffle</v-icon></v-btn>
        <v-btn flat icon class="mr-0" @click="favorite = !favorite" :color="favorite ? 'pink lighten-2' : 'white' "><v-icon>{{ favorite ? 'favorite' : 'favorite_outline' }}</v-icon></v-btn>
      </v-layout>
      <v-divider></v-divider>
      <div v-ripple>
      <v-layout row class="my-1">
        <v-layout column>
          <span>affection</span>
          <span class="grey--text">Jinsang</span>
        </v-layout>
        <v-spacer></v-spacer>
        <span class="my-auto">1:58</span>
      </v-layout>
      </div>
      <div v-ripple>
      <v-layout row class="my-1">
        <v-layout column>
          <span>Allien Boy</span>
          <span class="grey--text">Oliver Tree</span>
        </v-layout>
        <v-spacer></v-spacer>
        <span class="my-auto">2:44</span>
      </v-layout>
      </div>
      <div v-ripple>
      <v-layout row class="my-1">
        <v-layout column>
          <span>5:32pm</span>
          <span class="grey--text">The Deli</span>
        </v-layout>
        <v-spacer></v-spacer>
        <span class="my-auto">2:17</span>
      </v-layout>
      </div>
      <div v-ripple>
      <v-layout row class="my-1">
        <v-layout column>
          <span>Magic</span>
          <span class="grey--text">Yung Gravy</span>
        </v-layout>
        <v-spacer></v-spacer>
        <span class="my-auto">2:58</span>
      </v-layout>
      </div>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      play: true,
      loop: false,
      shuffle: false,
      favorite: false
    }
  }
}
</script>

<style media="screen">
  @import url('https://fonts.googleapis.com/css?family=Montserrat:900');
  @import url('https://fonts.googleapis.com/css?family=Monoton&display=swap');
  @import url('https://fonts.googleapis.com/css?family=Faster+One&display=swap');
  * {
    font-family: 'Montserrat';
  }
  ::-webkit-scrollbar{
    width: 0;
  }
  .round1 {
    border-radius: 1em;
  }
  .round2 {
    border-radius: 2em;
  }
  .height {
    height: 100%;
  }
  .width {
    width: 100%;
  }
  .center {
    margin-left: 50%;
    margin-top: 50%;
    transform: translate(-50%, -50%);
  }
  .center-abs {
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  .absolute {
    position: absolute;
  }
  .fixed {
    position: fixed;
  }
  .controls{
    z-index: 2;
  }
  .controls > *{
    opacity: 0;
    transition-duration: 0.5s;
    transition-property: all;
  }
  .cover{
    transition-duration: 0.5s;
    transition-property: all;
  }
  .controls:hover ~ .cover{
    filter: brightness(70%);
  }
  .controls:hover > *{
    opacity: 1;
  }
</style>
