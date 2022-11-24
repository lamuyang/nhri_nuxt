<template>
  <v-app>
      <v-app-bar app height="80" flat fixed color="rgba(206, 206, 206 ,1)">
        <v-spacer />
            <v-img
            class="mr-2"
            :src="require(`~/assets/logo/logo3.svg`)"
            max-width="400"
            contain
            />
            <!-- <v-toolbar-title class="primary--text text--darken-2 font-weight-black" v-text="title" style="font-family: TaipeiSans;" /> -->
          <v-spacer />
        <!-- <v-spacer />
        <v-row>
          <v-col cols="1">
            <v-img
            class="mr-2"
            :src="require(`~/assets/logo/logo.svg`)"
            max-width="100"
            contain
            />
          </v-col>
          <v-col cols="auto">
            <v-row>
            <v-toolbar-title class="primary--text text--darken-2 font-weight-black" v-text="title" style="font-family: TaipeiSans; font-size: 2rem;" />
            </v-row>
            <v-row>
              <v-toolbar-title class="primary--text text--darken-2 font-weight-black" v-text="eng_title" style="font-family: TaipeiSans;  font-size: 1rem;" />
            </v-row>
          </v-col>
      </v-row>
      <v-spacer /> -->
      </v-app-bar>
      <v-main>
        <v-container>
          <Header />
          <nuxt/>
        </v-container>
      </v-main>
      <Footer />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: "台灣基因檢測與風險預測平台",
      eng_title: "Taiwan Genetic test and Risk Prediction Platform"
    }
  },
}
</script>

<style>
#app {
    background-color: var(--v-background-base);
}
</style>