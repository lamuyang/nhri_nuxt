<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
      <v-img
        :src="require(`~/assets/img/TPMI.png`)"
        max-width="250"
        contain
        style="margin: auto"
      />
      <v-card-title style="font-size: ;">{{ article.title}}</v-card-title>
      <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle>
      <v-divider></v-divider>
      <v-card-title>{{ article.title}}</v-card-title>
      <v-card-text>{{ article.content }}</v-card-text>
      <v-card-text>{{ article.content }}</v-card-text>
      <v-card-title>{{ article.title}}</v-card-title>
      <v-card-text>{{ article.content }}</v-card-text>
    </v-card>
  </div>
</template>
<script>
export default {
  name: 'LatestNews',
  data() {
    return {
    }
  },
  async asyncData({ $axios }) {
    const article = await $axios.$post(`/LatestNews/2`)
    return {
      article
    }
  },
}
</script>