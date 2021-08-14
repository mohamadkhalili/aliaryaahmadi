<template>
  <v-card
    class="mx-auto overflow-hidden"
    width="100%"
  >
    <v-app-bar
      :color="color_p"
      prominent
      height="60px"
      :style="'direction: ' + $t('direction')"
    >
      <v-app-bar-nav-icon :color="color_s" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <div style="height: 48px; margin-inline: 4px; margin-top: 4px">
        <nuxt-link :to="switchLocalePath('fa')" :style="'text-decoration: none; font-size:16px;color: '+color_s" :hidden="this.$t('direction')=='rtl' ? true : false">فارسی</nuxt-link>
        <nuxt-link :to="switchLocalePath('en')" :style="'text-decoration: none; font-size:16px;color: '+color_s" :hidden="this.$t('direction')!='rtl' ? true : false">English</nuxt-link>
      </div>

      <v-spacer></v-spacer>

      <v-btn href="https://www.instagram.com/aliaryaahmadian/" icon>
        <v-icon :color="color_s">mdi-instagram</v-icon>
      </v-btn>

      <v-btn href="http://t.me/aliahmadianguitar" icon>
        <v-icon :color="color_s">mdi-telegram</v-icon>
      </v-btn>

      <v-btn href="https://www.youtube.com/channel/UCcJUKZX6R-g9dSm9g52j7JQ" icon>
        <v-icon :color="color_s">mdi-youtube</v-icon>
      </v-btn>

      <v-btn href="mailto: ali.ahmadian.m@gmail.com" icon>
        <v-icon :color="color_s">mdi-email</v-icon>
      </v-btn>

      <v-btn href="https://www.aparat.com/ALIARYAAHMADIAN/ALIARYAAHMADIAN" icon>
        <v-img :color="color_s" src="/aparat.svg" height="25px" width="25px" contain></v-img>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      class="deep-purple accent-4"
      :color="color_p"
      app
      fixed
      style="z-index: 100 !important;"
      temporary
      :right="this.$t('direction')=='rtl' ? true : false"
      height="100vh"
    >
      <v-list
        nav
        dense
      >
        <v-list-item
          v-model="group"
          v-for="item in $t('items')"
          :key="item.title"
          :to="($t('direction')=='rtl' ? '' : '/en/')+item.url"
        >
          <!--          <v-list-item-icon>-->
          <!--            <v-icon :color="color_s">{{ item.icon }}</v-icon>-->
          <!--          </v-list-item-icon>-->

          <v-list-item-content>
            <v-list-item-title :style="'text-align: ' + ($t('direction')=='rtl' ? 'right' : 'left')" :color="color_s">{{
                item.title
              }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <div style="width: 100% !important;height: calc(100% - 350px);padding-top: calc(40vh - 60px)"> <nuxt-link to="/#"><v-img width="120px" style="margin-left: auto;margin-right: auto;margin-top: auto" src="/logo.jpg"></v-img></nuxt-link></div>

    </v-navigation-drawer>
    <v-main id="main">
      <Nuxt/>
    </v-main>
  </v-card>
</template>

<script>
import Header from "./Header";

export default {
  components: {Header},
  data() {
    return {
      ffff: this.$t('right'),
      color_p: "#edefe5",
      color_s: "#006064",
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style>
.v-overlay {
  height: 100vh;
}
#main > .v-main__wrap {
  background: url('/background.jpg') no-repeat center center fixed !important;
  background-size: cover;
  position: static;
}
.v-overlay__scrim , .v-overlay{
  z-index: 90 !important;
}
</style>
