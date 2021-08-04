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

      <v-btn icon>
        <v-icon :color="color_s">mdi-instagram</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon :color="color_s">mdi-telegram</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon :color="color_s">mdi-youtube</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon :color="color_s">mdi-email</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon :color="color_s">mdi-podcast</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      class="deep-purple accent-4"
      :color="color_p"
      absolute
      :right="this.$t('direction')=='rtl' ? true : false"
      temporary
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

    </v-navigation-drawer>
    <v-main>
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
      color_p: "#FFCA28",
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
