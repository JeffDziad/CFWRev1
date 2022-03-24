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
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/rates" class="page_btn" @click="closeDrawer">
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="!hover" :src="rates"></v-img>
                    </transition>
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="hover" :src="rates_hover"></v-img>
                    </transition>
                  </v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" style="border: #f17105 solid 2px !important;" color="primary" width="150"><span>Rates and Terms</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/cottages" class="page_btn" @click="closeDrawer">
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="!hover" :src="cottages"></v-img>
                    </transition>
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="hover" :src="cottages_hover"></v-img>
                    </transition>
                  </v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" style="border: #f17105 solid 2px !important;" color="primary" width="150"><span>Cottages</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/contact" class="page_btn" @click="closeDrawer">
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="!hover" :src="contact"></v-img>
                    </transition>
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="hover" :src="contact_hover"></v-img>
                    </transition>
                  </v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" style="border: #f17105 solid 2px !important;" color="primary" width="150"><span>Contact Us!</span></v-card></v-col>
            </v-row>
          </v-col>
          <v-col align="center">
            <v-row>
              <v-col>
                <v-hover v-slot="{hover}">
                  <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/activities" class="page_btn" @click="closeDrawer">
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="!hover" :src="activities"></v-img>
                    </transition>
                    <transition mode="in-out" enter-active-class="animate__animated animate__fadeIn">
                      <v-img v-show="hover" :src="activities_hover"></v-img>
                    </transition>
                  </v-btn>
                </v-hover>
              </v-col>
            </v-row>
            <v-row>
              <v-col><v-card shaped class="white--text" style="border: #f17105 solid 2px !important;" color="primary" width="150"><span>Activities</span></v-card></v-col>
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
      activities: require('../assets/icons/page_icons/activities.png'),
      activities_hover: require('../assets/icons/page_icons/activities_hover.png'),
      cottages: require('../assets/icons/page_icons/cabins.png'),
      cottages_hover: require('../assets/icons/page_icons/cabins_hover.png'),
      contact: require('../assets/icons/page_icons/contact.png'),
      contact_hover: require('../assets/icons/page_icons/contact_hover.png'),
      rates: require('../assets/icons/page_icons/rates.png'),
      rates_hover: require('../assets/icons/page_icons/rates_hover.png')
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