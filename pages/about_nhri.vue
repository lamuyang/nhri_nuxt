<template>
    <div>
    <v-card elevation="2" outlined class="mt-5">
        <v-img
          :src="require(`~/assets/img/front.jpg`)"
          />
        <v-card-title>國家衛生研究院 National Health Research Institutes</v-card-title>
        <!-- <v-card-subtitle>{{ article.subtitle }}</v-card-subtitle> -->
        <v-divider></v-divider>
        <v-card-text>國家衛生研究院，簡稱國衛院，是中華民國在臺灣的一所非營利性醫藥與衛生研究機構，屬於公設的財團法人。位在苗栗縣竹南鎮，屬於新竹科學園區的一部分。最早的成立構想是在1988年，1996年依《財團法人國家衛生研究院設置條例》正式成立。創立基金來自政府捐助，每年運作的主要經費亦來自政府（衛生福利部）。</v-card-text>
        <v-card-title>簡介</v-card-title>
        <v-card-text>自1996 年1 月1 日成立以來，就以任務導向之醫藥衛生研究為目標，以增進國人健康福祉、提升醫藥衛生水準、發展醫藥科技及培育醫學人才為宗旨。 立志以客觀、科學的角度，從事基礎到臨床之轉譯研究，解決國人重大疾病問題，進而發展國內生物科技研究，並積極進行衛生政策研究與知識轉譯。</v-card-text>
        <v-card-title>院史</v-card-title>
        <v-card-text>國家衛生研究院之濫觴為1988年中央研究院院士會議中，建議政府成立國家醫學研究中心；規劃小組於1991年開始推動「行政院衛生署整合性醫藥衛生科技研究計畫」業務；1994年7月設置「國家衛生研究院籌備處」，於1996年1月正式成立。為有效發揮功能及永續發展，於2004年搬遷至永久院址—新竹科學園區竹南基地，並於2007年9月成立國家衛生研究院南部癌症研究中心。</v-card-text>
        <v-card-title>宗旨</v-card-title>
        <v-list-item>
            <v-list-item-icon>
                <v-icon color="indigo">
                    mdi-circle-small
                </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
                <v-list-item-title>增進國人健康福祉</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
        <v-list-item>
            <v-list-item-icon>
                <v-icon color="indigo">
                    mdi-circle-small
                </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
                <v-list-item-title>提昇醫藥衛生水準</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
        <v-list-item>
            <v-list-item-icon>
                <v-icon color="indigo">
                    mdi-circle-small
                </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
                <v-list-item-title>發展醫藥科技</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
        <v-list-item>
            <v-list-item-icon>
                <v-icon color="indigo">
                    mdi-circle-small
                </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
                <v-list-item-title>培育醫學人才</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
        <v-card-text>以上文章節錄自：https://www.nhri.edu.tw</v-card-text>
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