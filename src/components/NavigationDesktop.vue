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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/rates" class="page_btn">
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
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Rates and Terms</span></v-card></v-col>
              </v-row>
            </v-col>
            <v-col align="center">
              <v-row>
                <v-col>
                  <v-hover v-slot="{hover}">
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/cottages" class="page_btn">
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
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Cottages</span></v-card></v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>
        <v-col align="center" style="position: relative;">
          <logo></logo>
        </v-col>
        <v-col align="center">
          <v-row>
            <v-col align="center">
              <v-row>
                <v-col>
                  <v-hover v-slot="{hover}">
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/contact" class="page_btn">
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
                <v-col><v-card shaped class="white--text" color="primary" width="150"><span>Contact Us!</span></v-card></v-col>
              </v-row>
            </v-col>
            <v-col align="center">
              <v-row>
                <v-col>
                  <v-hover v-slot="{hover}">
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/activities" class="page_btn">
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
import Logo from "@/components/Logo";
export default {
  name: "NavigationDesktop",
  components: {Logo},
  data: () => {
    return {
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
  computed: {

  }
}
</script>

<style scoped>
.page_btn {
  border: rgba(0, 0, 0, 0) solid 2px;
}
</style>