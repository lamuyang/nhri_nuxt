<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      v-if="isMobile"
      :mini-variant="false"
      :clipped="clipped"
      fixed
      app
    >
      <v-list
        dense
        nav
      >
        <v-list-item to="/latest_news">
          <v-list-item-content>
            <v-list-item-title>最新消息</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item to="/precision_medicine">
          <v-list-item-content>
            <v-list-item-title>精準醫療</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title>服務項目</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item to="/about_nhri" >
          <v-list-item-content>
            <v-list-item-title>檢驗單位</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title>諮詢專區</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item to="/personal_report" >
          <v-list-item-content>
            <v-list-item-title>個人專區</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
      <v-app-bar app height="80" flat fixed color="rgba(206, 206, 206 ,1)">
        <v-app-bar-nav-icon v-if="isMobile" @click.stop="drawer = !drawer" />
          <v-img
          class="mr-2"
          :src="require(`~/assets/logo/logo-01.svg`)"
          max-width="40"
          contain
          />
          <v-toolbar-title class="primary--text text--darken-2 font-weight-black" v-text="title" />
          <v-spacer />
          <Header v-if="!isMobile" />
      </v-app-bar>
      <v-main>
        <v-container class="mt-2" style="height: 100%">
          <nuxt/>
        </v-container>
      </v-main>
      <!-- <Footer /> -->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: "台灣基因檢測與風險預測平台",
      eng_title: "Taiwan Genetic test and Risk Prediction Platform",
      drawer: false,
      clipped: false,
    }
  },
  computed: {
    isMobile() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          // return true
        case 'sm':
        case 'md':
          return true
        case 'lg':
        case 'xl':
          return false
      }
    },
  }
}
</script>

<style>
#app {
    background-color: var(--v-background-base);
}
</style>