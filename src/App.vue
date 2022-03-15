<template>
  <v-app>
    <v-main>
      <navigation-desktop></navigation-desktop>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

import NavigationDesktop from "@/components/NavigationDesktop";
export default {
  name: 'App',
  components: {NavigationDesktop},
  data: () => ({

  }),
};
</script>

<style>

</style>