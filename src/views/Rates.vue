<template>
  <v-row>
    <v-col align="center">
      <v-card max-width="1100" elevation="10">
        <v-toolbar color="primary" flat dark>
          <v-toolbar-title>Vrbo Calendar</v-toolbar-title>
        </v-toolbar>
        <v-tabs vertical>
          <v-tab>Loyola Calendar</v-tab>
          <v-tab>Marquette Calendar</v-tab>
          <v-tab-item>
            <!-- Loyola -->
            <br>
            <iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&bgcolor=%23ffffff&ctz=America%2FChicago&title=Loyola%20Cottage&src=MGoyNzFhMmg1ZXRvdm9rN2Q3YmNsbmgxMWFiamMyMm9AaW1wb3J0LmNhbGVuZGFyLmdvb2dsZS5jb20&color=%238E24AA" style="border:solid 1px #777" width="800" height="600" frameborder="0" scrolling="no"></iframe>
          </v-tab-item>
          <v-tab-item>
            <!-- Marquette -->
            <br>
            <iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&bgcolor=%23ffffff&ctz=America%2FChicago&title=Marquette%20Cottage&src=NXQ4bGx2YmNuOW1rOGd2Njcwam0xaHM1cjRsYXRjc2JAaW1wb3J0LmNhbGVuZGFyLmdvb2dsZS5jb20&color=%23795548" style="border:solid 1px #777" width="800" height="600" frameborder="0" scrolling="no"></iframe>
          </v-tab-item>
        </v-tabs>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Rates"
}
</script>

<style scoped>

</style>