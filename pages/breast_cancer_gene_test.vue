<template>
    <div>
        <h1 class="mb-2">乳癌基因體檢測</h1>
        <v-timeline
            align-top
            :dense="$vuetify.breakpoint.smAndDown"
        >
            <v-timeline-item
            v-for="(item, i) in items"
            :key="i"
            color="primary darken-1"
            :icon="item.icon"
            fill-dot
            >
            <v-card
                color="teal darken-1"
                dark
            >
                <v-card-title class="text-h6">
                {{ item.title }}
                </v-card-title>
                <v-card-text class="white text--primary">
                <p>{{ item.content }}</p>
                </v-card-text>
            </v-card>
            </v-timeline-item>
        </v-timeline>
        <v-row class="mt-10" justify='center'>
            <v-card shaped tag="ul" hover max-width="80%">
                        <v-card-title>什麼是乳癌？</v-card-title>
                        <v-card-text tag="li" class="ml-2">乳癌是惡性腫瘤，由乳房內不正常的細胞病變、侵略並破壞乳房正常的組織而形成，多在女性身上發生，但也有男性曾確診罹患乳癌。</v-card-text>
                        <v-card-text tag="li" class="ml-2">早期的乳癌屬原位癌，即癌細胞侷限於乳管或乳房小葉，而未擴散至乳房其他組織或身體其他器官，故也稱為非侵入性乳癌。</v-card-text>
                        <v-card-text tag="li" class="ml-2">但乳癌細胞是有可能跟隨血液和淋巴系統，擴散至腋下淋巴腺，以及身體其他器官和組織，例如肺部、骨骼、肝臟及腦部等，甚至會威脅患者的生命，而已擴散的乳癌可稱為侵入性乳癌。</v-card-text>
            </v-card>
        </v-row>
        <v-row class="mt-5" justify='center'>
            <v-card shaped tag="ul" width="80%" hover>
                <v-card-title>常見的乳癌種類</v-card-title>
                <v-card-text tag="li" class="ml-2"><strong>原位乳管癌 (DCIS)：</strong>癌症侷限於乳管內而未擴散</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>原位乳小葉癌 (LCIS)：</strong>癌症侷限於乳小葉內而未有擴散</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>侵入性乳管癌 (IDC)：</strong>癌細胞從乳管開始，穿透乳管壁，侵入乳房其他組織，甚至擴散至身體其他器官</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>侵入性乳小葉癌 (ILC)：</strong>癌細胞從乳小葉開始，擴散至身體其他器官</v-card-text>
            </v-card>
        </v-row>
        <v-row class="mt-5" justify='center'>
            <v-card shaped tag="ul" max-width="80%" hover>
                <v-card-title>如何預防乳癌？</v-card-title>
                <v-card-subtitle>乳癌是少數可以自我檢查發現問題的癌症，愈早發現，就愈能提高治癒的機會，能主動預防，就是阻擋乳癌侵襲的第一道屏障。要預防乳癌，必須從生活習慣開始，適量運動、保持標準體重、定期檢查及增強對乳癌的認知。</v-card-subtitle>
                <v-card-text tag="li" class="ml-2"><strong>適量運動：</strong>每星期最少4小時</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>控制體重：</strong>避免過重或肥胖</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>學習紓減壓力：</strong>壓力可以打亂身體的荷爾蒙分泌，學習放鬆及積極正面，如感到壓力過大，應主動尋求協助</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>少喝酒：</strong>有研究指出，減少喝酒可降低罹患乳癌的機會</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>吃得健康：</strong>少吃動物性飽和脂肪，多吃含抗氧化功能、維生素C、維生素E和胡蘿蔔素等食物，如藍莓、草莓、芥蘭、菠菜、西蘭花和紅椒等，有助抵抗自由基</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>避免太晚生育</strong></v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>定期篩檢</strong></v-card-text>
                <v-card-text>* 運動：適量運動能加強心肺功能，促進血液循環，還能清除積聚在體內的廢物及脂肪，增強身體抵抗力從而減低患病機會；亦有研究顯示，每週維持3小時健步行走的人士，能減低患上乳患的風險</v-card-text>
            </v-card>
        </v-row>
        <v-row class="mt-5 mb-5" justify='center'>
            <v-card shaped tag="ul" max-width="80%" hover>
                <v-card-title>如何檢查？多久一次？</v-card-title>
                <v-card-subtitle>乳癌是少數可以自我檢查發現問題的癌症，愈早發現，就愈能提高治癒的機會，能主動預防，就是阻擋乳癌侵襲的第一道屏障。要預防乳癌，必須從生活習慣開始，適量運動、保持標準體重、定期檢查及增強對乳癌的認知。</v-card-subtitle>
                <v-card-text tag="li" class="ml-2"><strong>適量運動：</strong>每星期最少4小時</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>控制體重：</strong>避免過重或肥胖</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>學習紓減壓力：</strong>壓力可以打亂身體的荷爾蒙分泌，學習放鬆及積極正面，如感到壓力過大，應主動尋求協助</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>少喝酒：</strong>有研究指出，減少喝酒可降低罹患乳癌的機會</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>吃得健康：</strong>少吃動物性飽和脂肪，多吃含抗氧化功能、維生素C、維生素E和胡蘿蔔素等食物，如藍莓、草莓、芥蘭、菠菜、西蘭花和紅椒等，有助抵抗自由基</v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>避免太晚生育</strong></v-card-text>
                <v-card-text tag="li" class="ml-2"><strong>定期篩檢</strong></v-card-text>
                <v-card-text>* 運動：適量運動能加強心肺功能，促進血液循環，還能清除積聚在體內的廢物及脂肪，增強身體抵抗力從而減低患病機會；亦有研究顯示，每週維持3小時健步行走的人士，能減低患上乳患的風險</v-card-text>
            </v-card>
        </v-row>
        <!-- <v-row>
            <v-col>
                <v-img 
                    :src="require(`~/assets/img/bc_2.png`)"
                    contain
                    max-width="350"
                ></v-img>
            </v-col>
        </v-row> -->
    </div>
</template>
<script>
  export default {
    data: () => ({
      items: [
        {
          color: 'teal darken-1',
          icon: 'mdi-small-circle',
          title: "檢驗前諮詢",
          content: '進行檢驗前會與受檢者進行相關諮詢，說明檢測內容與檢測流程。',
        },
        {
          color: 'teal darken-1',
          icon: 'mdi-small-circle',
          title: "採檢檢體",
          content: '7天內會收到使用說明書，至合作醫院或診所進行血液抽樣，而後樣品會統一由醫院密封寄回國衛院。',
        },
        {
          color: 'teal darken-1',
          icon: 'mdi-small-circle',
          title: "進行全基因定序",
          content: '使用NovaSeq 6000多功能定序儀，44小時內即可完成8-48人的全基因定序，並將資料匯入資料庫進行分析。',
        },
        {
          color: 'teal darken-1',
          icon: 'mdi-small-circler',
          title: "進行疾病風險評估",
          content: '使用專為台灣人建置的模型針對不同疾病分析基因與疾病的關係，最後產出報告，再交由醫院醫師向病人解說報告。',
        },
      ],
    }),
  }
</script>