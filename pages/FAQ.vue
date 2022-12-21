<template>
    <div>
        <template>
            <v-row justify="center" v-for="item in Q_A">
                <v-expansion-panels hover flat focusable class="mt-2">
                <v-expansion-panel>
                    <v-expansion-panel-header>{{ item.Q }}</v-expansion-panel-header>
                    <v-expansion-panel-content>{{ item.A }}</v-expansion-panel-content>
                </v-expansion-panel>
                </v-expansion-panels>
            </v-row>
        </template>
  </div>
</template>
<script>
export default {
  name: 'LatestNews',
  data() {
    return {
        Q_A:[
            {
                Q:"精準醫療的優點？",
                A:"提升用藥安全及效能，早期診斷及疾病預防，提供個人化健康管理。"
            },
            {
                Q:"是怎麼進行風險評估的?",
                A:"將基因定序後的數據先進行一些資料前處理，篩選掉品質不佳的資料，與疾病高相關性的位點進行比對，再透過PRS風險計算公式，計算出風險分數，我們會以該分數的高低來評估這個人對於該疾病的風險高低。"
            },{
                Q:"一般的基因定序跟全基因定序差別在哪裡?",
                A:"全基因定序比起基因定序能夠檢測出更多不同規模的變異，且全基因定序的技術門檻較高，能與市場表現出差異。"
            },{
                Q:"我的問題沒有列出的話，該怎麼辦呢？",
                A:"歡迎於平日上班時間 9:00-17:00 致電 國家衛生研究院 分子基因研究所 02-12344321 #123 "
            }
        ]
    }
  },
}
</script>