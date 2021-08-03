<template>

  <div id="cropper">
    <v-img id="main_img" :height="height+'%'" src="/main-img.jpg" style="background-position-x: right !important;background-position-y: top !important;"
           aspect-ratio="1.1">


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
      big_main_title: "top: 50%;position: absolute !important;right: 30%;width: 800px;text-align: center;color: #FFFFFF;font-size: 60px;line-height:1.5"
    }
  },
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return 50
        case 'sm':
          return 50
        case 'md':
          return 50
        case 'lg':
          return 100
        case 'xl':
          return 100
      }
    },
    style_main_title() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return this.big_main_title
        case 'sm':
          return this.big_main_title
        case 'md':
          return "width: 800px;text-align: center;color: #000000;font-size: 60px;line-height:1.8;"
        case 'lg':
          return "top: 50%;position: absolute !important;right: 40%;width: 800px;text-align: center;color: #FFFFFF;font-size: 60px;line-height:1.8;"
        case 'xl':
          return "top: 40%;position: absolute !important;right: 50%;width: 800px;text-align: center;color: #FFFFFF;font-size: 60px;line-height:1.9;"
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
  background-position-x: right !important;
}
</style>
