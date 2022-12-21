<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
      <v-img
        :src="require(`~/assets/img/1.jpg`)"
      />
      <v-card-title>{{ article.title}}</v-card-title>
      <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle>
      <v-divider></v-divider>
      <v-card-title>何謂基因定序?</v-card-title>
      <v-card-text>在細胞核裡的遺傳物質，就像程式碼決定程式的功能一樣，設定了生物的外觀、功能以及傾向。而人類的 DNA 若以字母書寫下來， 約會有 30 億個字母長，組成約 6 萬個基因，包含了 2 萬個會製造蛋白質的基因。</v-card-text>
      <v-card-text>全基因體定序(whole genome sequencing)便是將細胞核裡的 DNA 攤開來，抄寫成一部密密麻麻的天書。電腦軟體會將受檢者的定序資料，與參考基因組(reference genome)對照後找出不同處(或稱為變異 variant)，分析人員會進而比對這樣的不同是否與受檢者的臨床表現相符，以確認變異的致病性。全外顯子定序 (whole exome sequencing)則只分析會編碼成蛋白質的部分，而單基因定序(single gene sequencing)則只分析單一基因的序列。}</v-card-text>
      <v-card-title>找到致病基因的益處</v-card-title>
      <v-card-text>{對於難以解釋、不知如何治療的病症，若能找到受檢者致病的基因變異，便有機會了解致病機轉，主要好處有三：</v-card-text>
      <v-card-text>1. 精準化醫療:有些疾病會有特定的治療方式，了解致病機轉， 才能對症下藥。在急重難症的應用數據，可以用 2019 年的文獻說明，臺大醫院基因醫學部過去的經驗，約有一半的個案(40 位病童中的 21 位)能藉由一家三口全外顯子定序(同時分析患者及雙親的外顯子 DNA 序列)找到致病原因，而在這些人之中，又有一半(21 位中的 10 位)能找到特殊的治療方式。另外以苯酮尿症(phenylketonuria)為例，此症患者因代謝苯丙胺酸的能力先天缺陷，有毒物質在體內堆積，長久下來將造成漸進且不可回復的神經傷害。此症可粗分為飲食型及藥物型，飲食型需嚴格管控飲食中苯丙胺酸的量，而藥物型大多只需服用特定藥物即可。兩種類型的血漿苯丙胺酸都會升高，但致病機轉及治療方式卻南轅北轍，而代謝檢驗及基因檢測，能協助我們鑑別疾病的類型，以提供更精確的治療。</v-card-text>
      <v-card-text>2. 預測疾病進程:能參考過去文獻，了解其他擁有類似基因變異的人，除了已知的臨床表現以外，還有什麼症狀、徵候，可能 在現在或未來發生。</v-card-text>
      <v-card-text>3. 進行遺傳諮詢在患者的致病基因變異找到之後，可依照遺傳模式，推測哪些親屬可能帶有同樣基因變異，有潛在健康風險，須安排基因檢驗或其他檢查;另外，若父母希望避免再懷上患有同樣疾病的孩子，也可和醫師詢問討論下一胎的產前檢測方式。 </v-card-text>
      <v-card-title>基因檢測結果的灰色地帶</v-card-title>
      <v-card-text>在判讀定序資料時，可能發現明確致病的變異、明確不致病的變
異，以及未知臨床意義的變異。</v-card-text>
      <v-card-text>就像在判讀 DNA 這本天書時，可能會發現，「臺大醫院」寫成「臺 『太』醫院」，DNA 的意義完全改變;若是「臺」寫成「台」，則意義不變，並不改變基因功能。然而，更常見的狀況是，以現有 知識尚無法理解意義的變異。如遇到這種狀況，建議可每半年至一 年回診，再以更新的資料庫重新分析。</v-card-text>
      <v-card-title>偶然發現(incidental finding)</v-card-title>
      <v-card-text>基因定序時可能會發現和目標疾病表現無關的基因變異。除非該變異相關疾病是致命性的、在症狀出現前無法診斷，而且病程可以預 防或治療，否則目前此結果不會出現在報告上。另外，如果未來出現了新的症狀，懷疑其他遺傳疾病，也可以回診與您的醫師討論，是否需要重新分析。</v-card-text>
      <v-card-title>結語</v-card-title>
      <v-card-text>綜上所述，在基因定序找到致病基因變異後，對患者而言，能協助釐清疾病原因，以及時給予相對應治療，並預測疾病走向;對家族而言，可進一步尋找有風險的家屬，或對下一胎的計畫做諮詢。臺大醫院(總院及分院)的基因醫學部/小兒遺傳科門診有提供相關遺傳檢驗(本院提供全外顯子定序、一家三口全外顯子定序，以及全基因體定序等項目，亦可針對單一基因遺傳疾病做檢驗)。有相關需求的民眾可至門診接受遺傳諮詢，並與醫師討論是否安排檢驗。</v-card-text>
      <v-card-text>以上文章節錄自：https://epaper.ntuh.gov.tw/health/202208/project_1.html</v-card-text>
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
    const article = await $axios.$post(`/LatestNews/1`)
    return {
      article
    }
  },
}
</script>