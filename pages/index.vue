<template>

  <div id="cropper"  style="height:calc(100vh - 60px) !important;">
    <v-img id="main_img" :height="height+'%'" :src="main_img" style="background-position-x: center !important;background-position-y: center !important;"
           aspect-ratio="1.8">


    </v-img>

    <h1 class="text-center" color="#CDDC39" :style="style_main_title">
      {{ $t('main_title') }}
    </h1>
  </div>

</template>

<script>
export default {
  data() {
    return {

    }
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
          return "top: 40%;position: absolute !important;right: 3%;width: 340px;text-align: center;color: #FFCA28;font-size: 35px;line-height:1.8;font-family: vazir_o !important;"
        case 'sm':
          return "top: 40%;position: absolute !important;right: 10%;width: 580px;text-align: center;color: #FFCA28;font-size: 45px;line-height:1.8;font-family: vazir_o !important;"
        case 'md':
          return "top: 40%;position: absolute !important;right: 10%;width: 850px;text-align: center;color: #FFCA28;font-size: 60px;line-height:1.8;font-family: vazir_o !important;"
        case 'lg':
          return "top: 50%;position: absolute !important;right: 32%;width: 850px;text-align: center;color: #FFFFFF;font-size: 60px;line-height:1.8;font-family: vazir_o !important;"
        case 'xl':
          return "top: 40%;position: absolute !important;right: 50%;width: 850px;text-align: center;color: #FFFFFF;font-size: 60px;line-height:1.9;font-family: vazir_o !important;"
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
