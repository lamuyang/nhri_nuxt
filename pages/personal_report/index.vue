<template>
    <div>
        <v-card v-for="title in titles"  v-bind:key="title.title" class="mt-5">
            <v-card-title>{{ title.title }}</v-card-title>
            <!-- <v-card-actions v-if="!isMobile">
                <v-btn
                    outlined
                    shaped  
                    large
                    color="teal"
                    :to="`/personal_report/${title.low_file_name}`"
                >
                {{ title.low }}
                </v-btn>
                <v-btn
                    outlined
                    shaped  
                    large
                    color="yellow darken-1"
                    :to="`/personal_report/${title.mid_file_name}`"
                >
                {{ title.mid }}
                </v-btn>
                <v-btn
                    outlined
                    shaped
                    large
                    color="red darken-1"
                    :to="`/personal_report/${title.high_file_name}`"
                >
                {{ title.high }}
                </v-btn>
            </v-card-actions> -->
            <v-card-actions>
                <v-btn
                    outlined
                    shaped
                    large
                    color="teal"
                    class="mr-2"
                    @click="download(`${title.low_file_name}`)"
                >
                {{ title.low }}
                </v-btn>
            </v-card-actions>
            <v-card-actions>
                <v-btn
                    outlined
                    shaped
                    large
                    color="yellow darken-1"
                    class="mr-2"
                    @click="download(`${title.mid_file_name}`)"
                >
                {{ title.mid }}
                </v-btn>
            </v-card-actions>
            <v-card-actions>
                <v-btn
                    outlined
                    shaped
                    large
                    color="red darken-1"
                    @click="download(`${title.high_file_name}`)"
                >
                {{ title.high }}
                </v-btn>
            </v-card-actions>
        </v-card>
    </div>
</template>
<script>
export default {
    data() {
        return {
            titles:[
                {
                    title:"乳癌基因風險報告",
                    low:"低風險報告",
                    low_file_name:"BC_low",
                    mid:"中風險報告",
                    mid_file_name:"BC_mid",
                    high:"高風險報告",
                    high_file_name:"BC_high",
                },
                {
                    title:"高血壓基因風險報告",
                    low:"低風險報告",
                    low_file_name:"hy_low",
                    mid:"中風險報告",
                    mid_file_name:"hy_mid",
                    high:"高風險報告",
                    high_file_name:"hy_high",
                },
            ]
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
    computed: {
    isMobile() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
            return true
        case 'sm':
        case 'md':
        case 'lg':
        case 'xl':
        return false
      }
    },
  }
}
</script>