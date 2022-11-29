<template>
    <div>
        <v-card v-for="title in titles"  v-bind:key="title.title" class="mt-5">
            <v-card-title>{{ title.title }}</v-card-title>
            <v-card-actions v-if="!isMobile">
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
            </v-card-actions>
            <v-card-actions v-if="isMobile">
                <v-btn
                    outlined
                    shaped
                    large
                    color="teal"
                    class="mr-2"
                    :to="`/personal_report/${title.low_file_name}`"
                >
                {{ title.low }}
                </v-btn>
            </v-card-actions>
            <v-card-actions v-if="isMobile">
                <v-btn
                    outlined
                    shaped
                    large
                    color="yellow darken-1"
                    class="mr-2"
                    :to="`/personal_report/${title.mid_file_name}`"
                >
                {{ title.mid }}
                </v-btn>
            </v-card-actions>
            <v-card-actions v-if="isMobile">
                <v-btn
                    outlined
                    shaped
                    large
                    color="red darken-1"
                    :to="`/personal_report/${title.high_file_name}`"
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
                    low_file_name:"bc_low",
                    mid:"中風險報告",
                    mid_file_name:"bc_mid",
                    high:"高風險報告",
                    high_file_name:"hy_high",
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
    computed: {
    isMobile() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
            return true
        case 'sm':
            return false
        case 'md':
        case 'lg':
        case 'xl':
      }
    },
  }
}
</script>