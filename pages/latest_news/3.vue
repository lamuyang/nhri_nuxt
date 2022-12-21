<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
      <v-img
        :src="require(`~/assets/img/3.jpg`)"
        contain
      />
      <v-card-title>{{ article.title}}</v-card-title>
      <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle>
      <v-divider></v-divider>
      <v-card-text>國際巨星安潔莉娜．裘莉因母親罹患乳癌，且祖母、母親、阿姨皆相繼罹患乳癌過世，因此決定進行基因檢測。果然發現體內帶有BRCA1基因突變，這表示未來罹患乳癌機率高達87％，於是採取了預防性乳腺摘除手術，積極防治乳癌的發生。</v-card-text>
      <v-card-text>如果經濟條件許可，花大筆鈔票做基因檢測，以求檢查出未來可能會罹患哪些疾病，究竟值不值得？</v-card-text>
      <v-card-text>元鼎診所院長曾嶔元提醒，人類一生中可能罹患的疾病約有一萬兩千多種，隨著基因檢測的進步，透過分子生物學及基因體科學技術，針對個體基因排列、特定位點變異進行分析，可望找出未來可能發生的疾病。</v-card-text>
      <v-card-text>只是，生命極其複雜，基因檢測只能根據大數據法則找出與基因「低關聯度」、「中關聯度」和「高關聯度」的疾病。</v-card-text>
      <v-card-title>如何做？專業諮詢不能少</v-card-title>
      <v-card-text>在考慮是否進行基因檢測前，應該要先知道自己擔心哪些疾病發生，換句話說，檢測前的諮詢才是關鍵。他舉例，許多女性都會擔心罹患乳癌，那都該做檢測嗎？當然不是，應扣緊家族病史，如果個案的外婆、母親、阿姨或姊妹曾罹患乳癌，才有檢測的必要性。</v-card-text>
      <v-card-text>又例如阿茲海默症，個案的父母是否罹患、發病年齡是重要指標，若「有罹患」，且發病年齡在六十五歲以前，屬於「早發性失智症」，表示具有家族遺傳性。這種情況，檢測目的是要看個案下一代是否想了解罹病的風險。</v-card-text>
      <v-card-text>至於晚發性失智症，檢測目的則是了解自己屬於何種風險等級，採取的預防措施也就有所不同。</v-card-text>
      <v-card-text>「簡單來說，想做基因檢測之前必須要有充分且完整的了解——檢測前的目的、檢測後採取的改善措施並願意執行，也就是檢測者會因報告結果，願意有不同因應措施，例如積極改變生活型態，如此才有檢測的必要。」曾嶔元表示，畢竟結果就是一翻兩瞪眼的答案，日子還是要繼續往前走，總不能看著報告自己嚇自己。</v-card-text>
      <v-card-title>何時測？成年就能進行</v-card-title>
      <v-card-text>人生第一次該做基因檢測的最佳時機點，則可在成年後愈早愈好。若因生活習慣不佳或職業等因素，成為罹患心血管疾病、癌症的高危險族群，在經濟條件許可下，也不妨規畫為自己安排一次基因檢測。
      </v-card-text>
      <v-card-text>值得注意的是，為了避免被保險人日後可能面臨難索償的窘境，檢測前應留意醫療險有所謂的等待期，被保險人在保單生效後，特定天數之內，保單條款載明的理賠疾病，保單不予理賠，必須在過了特定天數後，保障內容才會正式啟動。如住院日額型醫療險、實支實付型醫療險的等待期最長三十天；癌症險、重大疾病險等待期最長九十天。</v-card-text>
      <v-card-text>至於基因檢測該怎麼做？依據不同檢測項目，需採取不同檢體。通常透過抽血、口腔刷棒刮取口腔內黏膜細胞，採取檢體即可，等待報告期間約一個月。</v-card-text>
      <v-card-text>換言之，這份報告是風險預估，不是100％精準。低風險不代表永遠沒問題，高風險也不用太過憂慮，關鍵仍在於是否就此強化健康行為的驅動力。</v-card-text>
      <v-card-text>以上文章節錄自：https://www.businesstoday.com.tw/article/category/183029/post/202104070049/</v-card-text>
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
    const article = await $axios.$post(`/LatestNews/3`)
    return {
      article
    }
  },
}
</script>