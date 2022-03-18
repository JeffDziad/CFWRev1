<template>
  <v-row>
    <v-col align="center">
      <v-card max-width="800" elevation="10">
        <v-container>

          <v-col><p class="text-h3 text-left red-grad white--text">&nbsp;Activities</p></v-col>

          <p class="text-left indent">
            This quiet cabin in Northern Wisconsin is ideally located at the edge of a crystal-clear, all-sports recreation lake. Enjoy time with family and friends with fishing, swimming, boating and paddling on Fence Lake! From our private pier, you can explore the lake and its connecting bodies of water on a scenic 10-lake chain through the pristine Northwoods. The surrounding area is peppered with ATV and snowmobile trails, hiking and biking trails, and other outdoor activities. If you up for a little excitement, Camp Flambeau is only 4 miles from Lake of the Torches Casino!
          </p>
          <p class="text-left indent">
            Nearby, you can play tennis or shoot hoops on some well-kept outdoor sport courts. This Northwoods cottage is also close to excellent local shopping and dining in Minocqua, Woodruff and Lac du Flambeau — all within just 15 minutes’ drive. We especially recommend trying out one of Wisconsin’s famous and historic supper clubs. Other popular attractions in the region include the Lake of Torches Casino, Fred Sheer’s Lumberjack Show, the Island City Antique Market, the Wildwood Wildlife Park and Nature Center, and the Waswagoning Indian Village
          </p>

          <v-col><p class="text-h3 text-left orange-grad white--text">&nbsp;Helpful Links</p></v-col>

          <v-row>
            <v-col>
              <v-list-item v-for="(link, i) in web_links" :key="i" :href="link.url" target="_blank">
                <v-list-item-title><span class="font-weight-bold text-decoration-underline">{{link.str}}</span></v-list-item-title>
              </v-list-item>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Activities",
  data: function() {
    return {
      web_links: [
        {str: "Attractions near Minocqua", url: "https://www.tripadvisor.com/Attractions-g60100-Activities-Minocqua_Wisconsin.html"},
        {str: "Fence Lake Chain", url: "https://dnr.wi.gov/lakes/lakepages/LakeDetail.aspx?wbic=2323000"},
        {str: "Attractions near Lac Du Flambeau", url: "https://www.tripadvisor.com/Attractions-g60019-Activities-Lac_du_Flambeau_Wisconsin.html"},
        {str: "Winter Activities near Minocqua", url: "https://www.minocqua.org/things-to-do/outdoor-activities/trail-reports/"},
        {str: "Snowmobile Trails at your doorstep", url: "https://www.hornshoe.org/"},
      ]
    }
  }
}
</script>

<style scoped>
.indent {
  text-indent: 50px;
}
.red-grad {
  background: rgb(146,0,0);
  background: linear-gradient(90deg, rgba(146,0,0,1) 0%, rgba(255,255,255,0) 89%, rgba(0,212,255,0) 100%);
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
}
.orange-grad {
  background: rgb(241,113,5);
  background: linear-gradient(90deg, rgba(241,113,5,1) 0%, rgba(255,255,255,0) 89%, rgba(0,212,255,0) 100%);
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
}
.yellow-grad {
  background: rgb(230,194,41);
  background: linear-gradient(90deg, rgba(230,194,41,1) 0%, rgba(255,255,255,0) 89%, rgba(0,212,255,0) 100%);
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
}
</style>