<template>
  <v-app>
    <v-row no-gutters class="ma-2 ma-sm-5 ma-md-5 ma-lg-10 ma-xl-10" :style="style">
      <v-col
        class="mt-5"
        v-for="(Sheet, index) in Sheets"
        :key="index"
        cols="12"
        xs="12"
        sm="12"
        md="12"
        lg="12"
        xl="12"
      >
        <ListStyle1 :data="Sheet"/>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
import ListStyle1 from "../components/ListStyle1";
export default {
  name: "sheets",
  components: {ListStyle1},
  data(){
    return {
      Sheets: [
        {
          text: this.$t('Sheets.p1.text'),
          url: this.$t('Sheets.p1.url'),
        },
        {
          text: this.$t('Sheets.p2.text'),
          url: this.$t('Sheets.p2.url'),
        },
        {
          text: this.$t('Sheets.p3.text'),
          url: this.$t('Sheets.p3.url'),
        },
        {
          text: this.$t('Sheets.p4.text'),
          url: this.$t('Sheets.p4.url'),
        },
        {
          text: this.$t('Sheets.p5.text'),
          url: this.$t('Sheets.p5.url'),
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>
