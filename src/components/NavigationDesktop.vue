<template>
  <div id="header">
    <v-container fill-height fluid>
      <v-row justify="center">
        <v-col>
          <v-row>
            <v-col align="center">
              <v-row>
                <v-col><v-btn icon :width="nav_btn_size" :height="nav_btn_size" to="/rates"><v-icon :size="nav_icon_size" color="primary">mdi-currency-usd</v-icon></v-btn></v-col>
              </v-row>
              <v-row>
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Rates and Terms</span></v-card></v-col>
              </v-row>
            </v-col>
            <v-col align="center">
              <v-row>
                <v-col><v-btn icon :width="nav_btn_size" :height="nav_btn_size" to="/cottages"><v-icon :size="nav_icon_size" color="primary">mdi-home</v-icon></v-btn></v-col>
              </v-row>
              <v-row>
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Cottages</span></v-card></v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>
        <v-col align="center" style="position: relative;">
          <canvas ref="logo_canvas" style="position: absolute; top: 0; left: 0; width: 100%; height: 200px; z-index: 0"></canvas>
          <router-link to="/">
            <v-img ref="logo" :src="logo_src" width="500"></v-img>
          </router-link></v-col>
        <v-col align="center">
          <v-row>
            <v-col align="center">
              <v-row>
                <v-col><v-btn icon :width="nav_btn_size" :height="nav_btn_size" to="/contact"><v-icon :size="nav_icon_size" color="primary">mdi-email</v-icon></v-btn></v-col>
              </v-row>
              <v-row>
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Contact Us!</span></v-card></v-col>
              </v-row>
            </v-col>
            <v-col align="center">
              <v-row>
                <v-col><v-btn icon :width="nav_btn_size" :height="nav_btn_size" to="/activities"><v-icon :size="nav_icon_size" color="primary">mdi-sail-boat</v-icon></v-btn></v-col>
              </v-row>
              <v-row>
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Activities</span></v-card></v-col>
              </v-row>
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
      logo_src: require('@/assets/text_logo.png'),
      nav_btn_size: 125,
      nav_icon_size: 120,
      logo_ctx: null,
      logo_increment: 0.05,
    }
  },
  methods: {
    animate_logo() {
      let canvas = this.$refs.logo_canvas;
      let c = this.logo_ctx;
      c.clearRect(-5, 0, canvas.width, canvas.height);
      c.beginPath();
      c.moveTo(0, canvas.height - 20);
      for(let i = 0; i < canvas.width; i++) {
        c.lineTo(i-5, canvas.height - 20 + Math.sin(i * 0.05 + this.logo_increment) * 15 * Math.sin(this.logo_increment));
      }
      c.strokeStyle = 'blue';
      c.stroke();
      this.logo_increment += 0.005;
      requestAnimationFrame(this.animate_logo);
    }
  },
  mounted() {
    this.logo_ctx = this.$refs.logo_canvas.getContext('2d');
    this.animate_logo();
  },
  created() {
  },
  destroyed() {

  }
}
</script>

<style scoped>
#header {

}
</style>