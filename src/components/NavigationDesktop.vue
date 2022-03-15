<template>
  <div id="header">
    <v-container fill-height fluid>
      <v-row justify="center">
        <v-col>
          <v-row>
            <v-col align="center">
              <v-btn icon :width="nav_btn_size" :height="nav_btn_size"><v-icon :size="nav_icon_size" color="primary">mdi-currency-usd</v-icon></v-btn>
            </v-col>
            <v-col align="center">
              <v-btn icon :width="nav_btn_size" :height="nav_btn_size"><v-icon :size="nav_icon_size" color="primary">mdi-home</v-icon></v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col align="center"><v-img :src="logo_src" width="500"></v-img></v-col>
        <v-col align="center">
          <v-row>
            <v-col align="center">
              <v-btn icon :width="nav_btn_size" :height="nav_btn_size"><v-icon :size="nav_icon_size" color="primary">mdi-email</v-icon></v-btn>
            </v-col>
            <v-col align="center">
              <v-btn icon :width="nav_btn_size" :height="nav_btn_size"><v-icon :size="nav_icon_size" color="primary">mdi-sail-boat</v-icon></v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "NavigationDesktop",
  data: () => {
    return {
      sunset_long_src: require('@/assets/sunset_bg_long.png'),
      logo_src: require('@/assets/text_logo.png'),
      nav_btn_size: 150,
      nav_icon_size: 100,
    }
  }
}
</script>

<style scoped>
#header {
  height: 150px;
}
</style>