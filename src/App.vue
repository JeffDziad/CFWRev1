<template>
  <v-app style="background-color: #343D3F;">
    <v-main>
      <div id="overlay">
        <navigation-desktop v-show="!mobile_mode"></navigation-desktop>
        <navigation-mobile v-show="mobile_mode"></navigation-mobile>
        <br>
        <br>
        <transition  mode="out-in" enter-active-class="animate__animated animate__fadeInLeft" leave-active-class="animate__animated animate__fadeOutRight">
          <router-view/>
        </transition>
      </div>
      <v-img eager :src="sunset_long_src" style="position: absolute; height: 100vh; top: 0; left: 0; z-index: 0; width: 100%"></v-img>
    </v-main>
  </v-app>
</template>

<script>

import NavigationDesktop from "@/components/NavigationDesktop";
import NavigationMobile from "@/components/NavigationMobile";
export default {
  name: 'App',
  components: {NavigationMobile, NavigationDesktop},
  data: () => ({
    sunset_long_src: require('./assets/sunset_bg_long.png'),
    mobile_mode: false
  }),
  methods: {
    window_resize() {
      this.mobile_mode = innerWidth < 1235;
    }
  },
  created() {
    window.addEventListener('resize', this.window_resize);
    this.window_resize();
  },
  destroyed() {
    window.removeEventListener('resize', this.window_resize);
  }
};
</script>

<style>
#overlay {
  position: relative;
  z-index: 2;
  padding-bottom: 20px;
}
</style>