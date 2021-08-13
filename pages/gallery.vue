<template>
  <v-app style="background-color: #00000000 !important;">
    <v-row no-gutters class="ma-2 ma-sm-5 ma-md-5 ma-lg-10 ma-xl-10" :style="style">
      <v-col
        class="mt-5"
        v-for="(gallery, index) in Gallerys"
        :key="index"
        cols="12"
        xs="12"
        sm="12"
        md="6"
        lg="6"
        xl="4"
      >
        <CardStyle1 :data="gallery"/>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "gallery",
  data() {
    return {
      style: 'direction:' + this.$t('direction'),
      Gallerys: [
        {
          title: this.$t('Gallerys.p1.title'),
          title2: this.$t('Gallerys.p1.title2'),
          subtitle: this.$t('Gallerys.p1.subtitle'),
          text: this.$t('Gallerys.p1.text'),
          img: this.$t('Gallerys.p1.img'),
          url: this.$t('Gallerys.p1.url')
        },
        {
          title: this.$t('Gallerys.p2.title'),
          title2: this.$t('Gallerys.p2.title2'),
          subtitle: this.$t('Gallerys.p2.subtitle'),
          text: this.$t('Gallerys.p2.text'),
          img: this.$t('Gallerys.p2.img'),
          url: this.$t('Gallerys.p2.url')
        },
        {
          title: this.$t('Gallerys.p3.title'),
          title2: this.$t('Gallerys.p3.title2'),
          subtitle: this.$t('Gallerys.p3.subtitle'),
          text: this.$t('Gallerys.p3.text'),
          img: this.$t('Gallerys.p3.img'),
          url: this.$t('Gallerys.p3.url')
        },
        {
          title: this.$t('Gallerys.p4.title'),
          title2: this.$t('Gallerys.p4.title2'),
          subtitle: this.$t('Gallerys.p4.subtitle'),
          text: this.$t('Gallerys.p4.text'),
          img: this.$t('Gallerys.p4.img'),
          url: this.$t('Gallerys.p4.url')
        },
        {
          title: this.$t('Gallerys.p5.title'),
          title2: this.$t('Gallerys.p5.title2'),
          subtitle: this.$t('Gallerys.p5.subtitle'),
          text: this.$t('Gallerys.p5.text'),
          img: this.$t('Gallerys.p5.img'),
          url: this.$t('Gallerys.p5.url')
        },
        {
          title: this.$t('Gallerys.p6.title'),
          title2: this.$t('Gallerys.p6.title2'),
          subtitle: this.$t('Gallerys.p6.subtitle'),
          text: this.$t('Gallerys.p6.text'),
          img: this.$t('Gallerys.p6.img'),
          url: this.$t('Gallerys.p6.url')
        },
        {
          title: this.$t('Gallerys.p7.title'),
          title2: this.$t('Gallerys.p7.title2'),
          subtitle: this.$t('Gallerys.p7.subtitle'),
          text: this.$t('Gallerys.p7.text'),
          img: this.$t('Gallerys.p7.img'),
          url: this.$t('Gallerys.p7.url')
        },
        {
          title: this.$t('Gallerys.p8.title'),
          title2: this.$t('Gallerys.p8.title2'),
          subtitle: this.$t('Gallerys.p8.subtitle'),
          text: this.$t('Gallerys.p8.text'),
          img: this.$t('Gallerys.p8.img'),
          url: this.$t('Gallerys.p8.url')
        },
        {
          title: this.$t('Gallerys.p9.title'),
          title2: this.$t('Gallerys.p9.title2'),
          subtitle: this.$t('Gallerys.p9.subtitle'),
          text: this.$t('Gallerys.p9.text'),
          img: this.$t('Gallerys.p9.img'),
          url: this.$t('Gallerys.p9.url')
        },
        {
          title: this.$t('Gallerys.p10.title'),
          title2: this.$t('Gallerys.p10.title2'),
          subtitle: this.$t('Gallerys.p10.subtitle'),
          text: this.$t('Gallerys.p10.text'),
          img: this.$t('Gallerys.p10.img'),
          url: this.$t('Gallerys.p10.url')
        },
        {
          title: this.$t('Gallerys.p11.title'),
          title2: this.$t('Gallerys.p11.title2'),
          subtitle: this.$t('Gallerys.p11.subtitle'),
          text: this.$t('Gallerys.p11.text'),
          img: this.$t('Gallerys.p11.img'),
          url: this.$t('Gallerys.p11.url')
        },
        {
          title: this.$t('Gallerys.p12.title'),
          title2: this.$t('Gallerys.p12.title2'),
          subtitle: this.$t('Gallerys.p12.subtitle'),
          text: this.$t('Gallerys.p12.text'),
          img: this.$t('Gallerys.p12.img'),
          url: this.$t('Gallerys.p12.url')
        },
      ]
    }
  },
}
</script>

<style scoped>

</style>
