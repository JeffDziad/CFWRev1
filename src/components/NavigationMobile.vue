<template>
  <div id="header">
    <v-btn icon x-large style="position: absolute; z-index: 2" @click="nav_drawer = !nav_drawer"><v-icon>mdi-menu</v-icon></v-btn>
    <transition mode="in-out" enter-active-class="animate__animated animate__fadeInDown" leave-active-class="animate__animated animate__fadeOutUp">
      <div v-show="nav_drawer" id="nav_menu">
        <v-btn absolute icon x-large style="position: relative" @click="nav_drawer = !nav_drawer"><v-icon>mdi-close</v-icon></v-btn>
        <v-row>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/rates" class="page_btn" @click="closeDrawer"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-currency-usd</v-icon></v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Rates and Terms</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/cottages" class="page_btn" @click="closeDrawer"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-home</v-icon></v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Cottages</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/contact" class="page_btn" @click="closeDrawer"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-email</v-icon></v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Contact Us!</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/activities" class="page_btn" @click="closeDrawer"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-sail-boat</v-icon></v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Activities</span></v-card></v-col>
            </v-row>
          </v-col>
        </v-row>
      </div>
    </transition>
    <v-container fill-height fluid>
      <v-row justify="center">
        <v-col align="center" style="position: relative;">
          <logo></logo>
        </v-col>
      </v-row>
    </v-container>

  </div>
</template>

<script>
import Logo from "@/components/Logo";
export default {
  name: "NavigationMobile",
  components: {
    Logo
  },
  data: () => {
    return {
      nav_drawer: false,
      nav_btn_size: 130,
      nav_icon_size: 120,
    }
  },
  methods: {
    closeDrawer() {
      this.nav_drawer = false;
    }
  }
}
</script>

<style scoped>
#nav_menu {
  padding: 10px;
  position: absolute;
  width: 100%;
  background-color: rgba(136,136,136,0.2);
  backdrop-filter: blur(30px);
  z-index: 5;
  box-shadow: 0px 10px 77px 4px rgba(0,0,0,0.75);
  -webkit-box-shadow: 0px 10px 77px 4px rgba(0,0,0,0.75);
  -moz-box-shadow: 0px 10px 77px 4px rgba(0,0,0,0.75);
}
</style>