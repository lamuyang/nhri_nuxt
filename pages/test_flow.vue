<template>
    <div>
        <h1 class="mb-2">全基因體檢測流程</h1>
        <v-timeline
            align-top
            :dense="$vuetify.breakpoint.smAndDown"
        >
            <v-timeline-item
            v-for="(item, i) in items"
            :key="i"
            color="teal darken-1"
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