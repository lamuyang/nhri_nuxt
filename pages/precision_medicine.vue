<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
        <v-img
          :src="require(`~/assets/img/PM.jpg`)"
          contain
          />
        <v-card-title>【什麼是】精準醫療Precision Medicine?</v-card-title>
        <!-- <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle> -->
        <v-divider></v-divider>
        <v-card-text>精準醫療是什麼?這個專有名詞和我們有什麼關係。事實上，你已經有接觸或知道精準醫療。例如說在病人需要輸血，我們都知道要配對血型，而不是隨便找一包血就可以輸血，這就是精準醫療概念的應用。但是到近幾年，我們才比較有聽到這樣的名詞。要和大家介紹這個名詞，因為有越來越多根據精準醫療的概念，所開發的醫療器材和基礎研究。</v-card-text>
        <v-card-title>精準醫療是什麼?</v-card-title>
        <v-card-text>精準醫療是將個人的基因、環境和生活型態都考慮進去的疾病治療和預防方法。因此，醫師和研究人員能針對特定疾病和族群，給予較更合適的治療和預防對策，對於預後能有較精確的預測。不再是一種治療方法適用所有人。因為普遍的醫療方法，起因適用平均或大部分的人，較少對個體和個體間的差異做考量。</v-card-text>
        <v-card-title>誰不想得到精準的治療?</v-card-title>
        <v-card-text>這讓人想到在臨床醫療上，抗生素使用的問題。因為臨床上無法快速檢測出患者受那一種細菌感染，每個人對抗生素的反應可能不同，而醫師又必須在有限的時間內做出治療的決定，時常不得以，給出一種萬用或嘗試性的抗生素，長期患者可能產生抗藥性，或者根本無法有效治療。而在癌症治療上，化療和標靶，有人做出來很有效，有人就沒效，即使有在治療前有了很多的檢測，依舊無法保證每個人都有效，當然臨床原因有很多種，不過這也讓精準醫療有很多的努力空間。</v-card-text>
        <v-card-title>精準醫療需要什麼?</v-card-title>
        <v-card-text>人和人之前有差異，生活環境、生活方式，甚至基因上有差異。要能掌握基因上的差異對醫療的影響，就非常需要基因資料庫。所以不但要有一套有效率能達成精準醫療的方法，還需要有完整強大的基因資料庫。就此衍伸出來，有人在專門治療開發方法，有人在蒐集建置資料庫。</v-card-text>
        <v-card-text>簡言之，精準醫療的本質，像是醫療版本的「因材施教」，而醫生就是老師，病患就是學生。而因材施教需要方法，各種精準醫療延伸出來的治療和預防技術，就是這些方法。當醫療方法更完善精準，我們就有機會接受到更有效率的治療。</v-card-text>
        <v-card-text>資料參考：https://medlineplus.gov/genetics/understanding/precisionmedicine/definition/</v-card-text>
        <v-card-text>以上文章節錄自：https://biomeder.com/what-is-precision-medicine/</v-card-text>
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
}
</script>