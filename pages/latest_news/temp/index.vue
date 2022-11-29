<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
      <v-card-title>{{ article.title}}</v-card-title>
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
  async asyncData({ params, $axios }) {
    const id = params.newsId
    console.log(id);
    const article = await $axios.$post(`/LatestNews/${id}`)
    // console.log(article);
    return {
      article, id
    }
  },
}
</script>