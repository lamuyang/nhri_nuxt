<template>
  <div>
    <div v-for="article in articleArr" v-bind:key="article.id">
      <v-card elevation="2" outlined class="mt-5">
        <v-card-title class="h1">{{ article.title }}</v-card-title>
        <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle>
        <v-card-text>{{ article.abstract }}</v-card-text>
        <v-card-actions>
          <v-btn
            outlined
            rounded
            text
            :to="`/latest_news/${article.id}`"
          >
          查看全文
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
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
    const articleArr = await $axios.$post('/LatestNews')
    console.log(articleArr);
    return {
      articleArr,
    }
  },
}
</script>