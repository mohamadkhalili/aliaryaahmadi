<template>

  <div id="cropper" style="height:calc(100vh - 60px) !important;padding: 50px">
    <v-img id="main_img" :height="height+'%'" :src="main_img"
           style="background-position-x: center !important;background-position-y: center !important;"
           alt="علی آریا احمدیان"
           aspect-ratio="1.8">


    </v-img>

    <v-row style="width: auto;height: 20%;top: 0%;left: 0px;display: block;position: absolute; margin-top: 110px; max-width: 30%;margin-left: 55px">
      <v-col cols="12">
        <v-img width="120px" style="margin-left: auto;margin-right: auto;margin-top: auto" src="/logo.jpg"></v-img>
      </v-col>
      <v-col cols="12">
        <h1 class="text-center" color="#CDDC39" :style="style_main_title">
          {{ $t('main_title') }}
        </h1>
      </v-col>
      <v-col cols="12">
        <h4 class="text-center" color="#CDDC39" :style="style_main_subtitle">
          {{ $t('main_subtitle') }}
        </h4>
      </v-col>
    </v-row>
  </div>

</template>

<script>
export default {
  data() {
    return {}
  },
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return 100
        case 'sm':
          return 100
        case 'md':
          return 100
        case 'lg':
          return 100
        case 'xl':
          return 100
      }
    },
    main_img() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return "/main-small-img.jpg"
        case 'sm':
          return "/main-small-img.jpg"
        case 'md':
          return "/main-small-img.jpg"
        case 'lg':
          return "/main-img.jpg"
        case 'xl':
          return "/main-img.jpg"
      }
    },
    style_main_title() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return "text-align: center;color: #fdfff5;font-size: 15px;line-height:1.8;font-family: vazir_o !important;"
        case 'sm':
          return "text-align: center;color: #fdfff5;font-size: 20px;line-height:1.8;font-family: vazir_o !important;"
        case 'md':
          return "text-align: center;color: #fdfff5;font-size: 25px;line-height:1.8;font-family: vazir_o !important;"
        case 'lg':
          return "text-align: center;color: #fdfff5;font-size: 35px;line-height:1.8;font-family: vazir_o !important;"
        case 'xl':
          return "text-align: center;color: #fdfff5;font-size: 40px;line-height:1.9;font-family: vazir_o !important;"
      }
    },
    style_main_subtitle() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return "text-align: center;color: #fdfff5;font-size: 7px;line-height:1.8;font-family: vazir_o !important;"
        case 'sm':
          return "text-align: center;color: #fdfff5;font-size: 10px;line-height:1.8;font-family: vazir_o !important;"
        case 'md':
          return "text-align: center;color: #fdfff5;font-size: 12px;line-height:1.8;font-family: vazir_o !important;"
        case 'lg':
          return "text-align: center;color: #fdfff5;font-size: 17px;line-height:1.8;font-family: vazir_o !important;"
        case 'xl':
          return "text-align: center;color: #fdfff5;font-size: 20px;line-height:1.9;font-family: vazir_o !important;"
      }
    },
  },
}
</script>


<style>
#cropper {
  width: 100%;
  height: 100%;
}

#cropper > div > .v-image__image {
  background-position-x: center !important;
  background-position-y: top !important;
}
</style>
