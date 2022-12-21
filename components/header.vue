<template>
    <div>
        <v-btn shaped x-large to="/latest_news" class="mr-2">
            最新訊息
        </v-btn>
        <v-btn shaped x-large to="/precision_medicine" class="mr-2">
            精準醫療
        </v-btn>
        <v-menu :close-on-content-click="false" open-on-hover bottom offset-y>
            <template v-slot:activator="{ on, attrs }">
                <v-btn shaped x-large v-bind="attrs" v-on="on" class="mr-2">
                    服務項目
                </v-btn>
            </template>
            <v-list dense>
                <v-list-group
                    v-for="item in items"
                    :key="item.title"
                >
                <template v-slot:activator>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </template>
              <v-list-item
                v-for="subItem in item.items"
                :key="subItem.title"
                :to="`${subItem.link}`"
              >
                <v-list-item-content>
                  <v-list-item-title>{{ subItem.title }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
          </v-list>
        </v-menu>
        <v-btn shaped x-large to="/FAQ" class="mr-2">
            諮詢專區
        </v-btn>
        <v-btn shaped x-large to="/login" class="mr-2">
            個人專區
        </v-btn>
        <v-btn shaped x-large to="/about_nhri" class="mr-2">
            聯絡我們
        </v-btn>
    </div>
</template>
    
<script>
export default {
    data: () => ({
        activate: true,
        theme: 1,
        themes: [{
                text: "Dark",
                icon: "mdi-clock"
            },
            {
                text: "Light",
                icon: "mdi-account"
            }
        ],
        mini: true,
        items: [{
                title: "乳癌基因體檢測",
                items: [
                    {
                        title: "認識乳癌",
                        link: "/about_breast_cancer"
                    },
                    {
                        title: "檢測流程",
                        link: "/test_flow"
                    }
                ]
            },
            {
                title: "高血壓基因體檢測",
                items: [
                    {
                        title: "認識高血壓",
                        link: "/about_hypertension"
                    },
                    {
                        title: "檢測流程",
                        link: "/test_flow"
                    }
                ]
            },
        ]
    })
};
</script>