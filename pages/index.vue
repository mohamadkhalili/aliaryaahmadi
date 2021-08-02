<template>

  <div id="cropper">
    <v-img id="main_img" :height="height+'%'" src="/main-img.jpg" style="background-position-x: right !important;" class="d-" aspect-ratio="1.8">


    </v-img>
  </div>

</template>

<script>
  export default {
    computed: {
      height () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 50
          case 'sm': return 50
          case 'md': return 50
          case 'lg': return 100
          case 'xl': return 100
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
