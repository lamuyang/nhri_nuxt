<template>
    <div>
        <v-btn shaped x-large to="/" class="mr-2">
            最新訊息
        </v-btn>
        <v-menu :rounded="rounded" open-on-hover offset-y transition="slide-y-transition" bottom right>
            <template v-slot:activator="{ on, attrs }">
                <v-btn shaped x-large v-bind="attrs" v-on="on" class="mr-2">
                    精準健康
                </v-btn>
            </template>
            <v-list dense>
                <v-list-item v-for="(item, index) in health" :key="index" router :to="item.link">
                    <v-list-item-action>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-action>
                </v-list-item>
            </v-list>
        </v-menu>
        <v-menu :rounded="rounded" open-on-hover offset-y transition="slide-y-transition" bottom right>
            <template v-slot:activator="{ on, attrs }">
                <v-btn shaped x-large v-bind="attrs" v-on="on" class="mr-2">
                    服務項目
                </v-btn>
            </template>
            <v-list dense>
                <v-list-item v-for="(item, index) in services" :key="index" router :to="item.link">
                    <v-list-item-action>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-action>
                </v-list-item>
            </v-list>
        </v-menu>
        <v-btn shaped x-large to="/contact" class="mr-2">
            檢驗單位
        </v-btn>
        <v-btn shaped x-large to="/contact" class="mr-2">
            諮詢專區
        </v-btn>
        <v-btn shaped x-large to="/contact" class="mr-2">
            個人專區
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
        services: [{
                icon: "mdi-domain",
                title: "乳癌基因體檢測",
                link: "/mmrservices"
            },
            {
                icon: "mdi-message-text",
                title: "高血壓基因體檢測",
                link: "/amrservices"
            },
        ],
        health: [{
                icon: "mdi-domain",
                title: "精準健康",
                link: "/mmrservices"
            },
            {
                icon: "mdi-message-text",
                title: "精準醫療",
                link: "/amrservices"
            },
        ]
    })
};
</script>