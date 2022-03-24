<template>
  <div id="header">
    <v-container fill-height fluid>
      <v-row justify="center">
        <v-col>
          <v-row>
            <v-col align="center">
              <v-row>
                <v-col>
                  <v-hover v-slot="{hover}">
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/rates" class="page_btn" @click="page_click">
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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/cottages" class="page_btn" @click="page_click">
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
          </v-row>
        </v-col>
        <v-col ref="logo_col" align="center" style="position: relative; margin-top: 200px; transition: all 2s;">
          <logo @logo_clicked="logo_click"></logo>
          <br>
          <br>
          <transition enter-active-class="animate__animated animate__zoomInUp" leave-active-class="animate__animated animate__zoomOut">
            <div ref="subtitle" v-show="atHome">
              <div id="logo_subtitle">
                <p style="font-size: 35px; font-family: 'Bungee', serif; z-index: 0;">A fun-filled and relaxing get-a-way on the shore of Fence Lake</p>
                <p style="font-size: 35px; font-family: 'Bungee', serif; z-index: 0;">A fun-filled and relaxing get-a-way on the shore of Fence Lake</p>
              </div>

            </div>
          </transition>

        </v-col>
        <v-col align="center">
          <v-row>
            <v-col align="center">
              <v-row>
                <v-col>
                  <v-hover v-slot="{hover}">
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/contact" class="page_btn" @click="page_click">
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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/activities" class="page_btn" @click="page_click">
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
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Logo from "@/components/Logo";
export default {
  name: "NavigationDesktop",
  components: {Logo},
  data: () => {
    return {
      nav_btn_size: 130,
      nav_icon_size: 120,
      atHome: false,
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
  computed: {

  },
  methods: {
    logo_click() {
      this.$refs.logo_col.style.marginTop = '200px';
      this.atHome = true;
    },
    page_click() {
      this.$refs.logo_col.style.marginTop = '0px';
      this.atHome = false;
    }
  },
  mounted() {
    if(this.$router.currentRoute.name.toUpperCase() === 'HOME') {
      this.atHome = true;
    } else {
      this.page_click();
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bungee&display=swap');

.page_btn {
  border: rgba(0, 0, 0, 0) solid 2px;
}

#logo_subtitle {
  position: relative;
}

#logo_subtitle p {
  position: absolute;
}

#logo_subtitle p:nth-child(1) {
  color: transparent;
  -webkit-text-stroke: 2px black;
}

#logo_subtitle p:nth-child(2) {
  color: #0076CE;
  animation: animate 25s ease-in-out infinite;
}

@keyframes animate {
  0%,
  100% {
    clip-path: polygon(
        0% 2%,
        16% 2%,
        33% 1%,
        70% 2%,
        100% 1%,
        100% 100%,
        120% 100%,
        120% 120%,
        0% 100%
    );
  }

  50% {
    clip-path: polygon(
        0% 120%,
        100% 100%,
        100% 100%,
        100% 100%,
        100% 100%,
        100% 100%,
        100% 100%,
        100% 100%,
        0% 100%
    );
  }
}
</style>