<template>
  <v-card
    class="mx-auto overflow-hidden"
    height="100vh"
    width="100%"
  >
    <v-app-bar
      color="#00000000"
      prominent
      height="60px"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>


      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-instagram</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-telegram</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-youtube</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-email</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-podcast</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      class="deep-purple accent-4"

      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item
          v-model="group"
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>
    <v-main style="height:calc(100% - 60px) !important;">
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
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
