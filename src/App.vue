<template>
  <v-app>
    <v-main>
      <v-img :src="sunset_long_src" style="position: absolute; top: 0; left: 0; z-index: 0; width: 100%"></v-img>
      <navigation-desktop></navigation-desktop>
      <transition  mode="out-in" enter-active-class="animate__animated animate__fadeInLeft" leave-active-class="animate__animated animate__fadeOutRight">
        <router-view/>
      </transition>
    </v-main>
  </v-app>
</template>

<script>

import NavigationDesktop from "@/components/NavigationDesktop";
export default {
  name: 'App',
  components: {NavigationDesktop},
  data: () => ({
    sunset_long_src: require('./assets/sunset_bg_long.png'),
  }),
};
</script>

<style>

</style>