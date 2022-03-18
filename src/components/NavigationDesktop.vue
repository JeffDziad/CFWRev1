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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/rates" class="page_btn"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-currency-usd</v-icon></v-btn>
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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/cottages" class="page_btn"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-home</v-icon></v-btn>
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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/contact" class="page_btn"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-email</v-icon></v-btn>
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
                    <v-btn rounded outlined :width="nav_btn_size" :height="nav_btn_size" to="/activities" class="page_btn"><v-icon :size="nav_icon_size" :color="(hover) ? 'secondary' : 'primary'">mdi-sail-boat</v-icon></v-btn>
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
    }
  },
}
</script>

<style scoped>
.page_btn {
  border: rgba(0, 0, 0, 0) solid 2px;
}
</style>