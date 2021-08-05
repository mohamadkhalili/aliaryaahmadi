<template>
  <v-card :href="data.url" class="ma-5" :max-width="height*2+'px'" :height="height+'px'" :style="'direction:' + this.$t('direction')">
    <v-row :style="'direction:' + this.$t('direction')+';max-height: 100%'">
      <v-col
        cols="4" class="pa-2" :style="'max-height: '+(height-10)+'px !important;'"
      >
        <v-img :src="data.img" style="margin: 5px;max-height: 100%"/>
      </v-col>
      <v-col
        cols="8"
      >
        <h2 class="mb-2">{{ data.title }}</h2>
        <h4 class="mb-6">{{ data.subtitle }}</h4>
        <h5>{{ data.text }}</h5>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: "WorkCard",
  data() {
    return {
      work: null
    }
  },
  props: {
    data: Object
  },
  watch: {
    data: {
      immediate: true,
      deep: true,
      handler(newV) {
        this.work = newV
      }
    },
  },
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return 250
        case 'sm':
          return 200
        case 'md':
          return 200
        case 'lg':
          return 300
        case 'xl':
          return 300
      }
    },
    width() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return 300
        case 'sm':
          return 200
        case 'md':
          return 200
        case 'lg':
          return 300
        case 'xl':
          return 300
      }
    },
  }
}
</script>

<style scoped>

</style>
