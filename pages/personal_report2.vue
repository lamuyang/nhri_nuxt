<template>
    <v-card>
        <v-toolbar>
            <v-toolbar-title>個人基因風險檢測報告檢視</v-toolbar-title>
            <v-btn
                outlined
                shaped
                large
                to="/login"
                class="ml-auto"
            >
            登出
            </v-btn>
        </v-toolbar>
        <v-row>
            <v-col cols="6">
                <v-card-title>基本資料</v-card-title>
                <v-form class="mt-10">
                    <v-row>
                        <v-col cols="3">
                            <v-subheader>姓名：</v-subheader>
                        </v-col>
                        <v-col cols="9">
                            <v-text-field
                                flat
                                v-model="name"
                                readonly
                                solo
                            ></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="3">
                            <v-subheader>性別：</v-subheader>
                        </v-col>
                        <v-col cols="9">
                            <v-text-field
                                flat
                                v-model="gender"
                                readonly
                                solo
                            ></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="3">
                            <v-subheader>出生年月日：</v-subheader>
                        </v-col>
                        <v-col cols="9">
                            <v-text-field
                                flat
                                v-model="date_of_birth"
                                readonly
                                solo
                            ></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="3">
                            <v-subheader>檢查編號：</v-subheader>
                        </v-col>
                        <v-col cols="9">
                            <v-text-field
                                flat
                                v-model="check_id"
                                readonly
                                solo
                            ></v-text-field>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
            <v-col cols="6">
                <v-card-title>報告下載</v-card-title>
                <v-form class="mt-10">
                    <v-row>
                        <v-col cols="6">
                            <v-subheader>乳癌基因風險檢測結果</v-subheader>
                        </v-col>
                        <v-col cols="6">
                            <v-text-field
                                flat
                                v-model="high"
                                readonly
                                solo
                                class="text-input-red"
                            ></v-text-field>
                            <v-card-actions>
                                <v-btn
                                    outlined
                                    shaped
                                    large
                                    color="red darken-1"
                                    @click="download('王阿花-乳癌基因風險檢測報告')"
                                >
                                報告下載
                                </v-btn>
                            </v-card-actions>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="6">
                            <v-subheader>高血壓基因風險檢測結果</v-subheader>
                        </v-col>
                        <v-col cols="6">
                            <v-text-field
                                flat
                                v-model="mid"
                                readonly
                                solo
                                class="text-input-red"
                            ></v-text-field>
                            <v-card-actions>
                                <v-btn
                                    outlined
                                    shaped
                                    large
                                    color="yellow darken-3"
                                    @click="download('王阿花-高血壓基因風險檢測報告')"
                                >
                                報告下載
                                </v-btn>
                            </v-card-actions>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-card>
</template>
<script>
export default {
    data() {
    return {
        name: '王阿花',
        gender: '生理女',
        date_of_birth: '2001/08/03',
        check_id: 'nhri000002',
        high: '高風險',
        mid: '中風險',
    }
  },
  methods:{
      async download(file_name) {
        this.$axios({
        url: `/download_personal_report/${file_name}.pdf`,
        method: 'POST',
        responseType: 'blob',
        }).then((response) => {
        const url = window.URL.createObjectURL(new Blob([response.data]));
        const link = document.createElement('a');
        link.href = url;
        link.setAttribute('download', file_name+".pdf");
        document.body.appendChild(link);
        link.click();
        });
      }
    },
}
</script>