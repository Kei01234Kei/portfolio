<template>
  <v-app app>
    <v-app-bar app color="white">
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title><router-link to="/">Keisuke Ishigami</router-link></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon href="https://github.com/Kei01234">
        <v-icon color="black">mdi-github</v-icon>
      </v-btn>
      <v-btn icon href="https://twitter.com/Kei01234Kei">
        <v-icon color="blue">mdi-twitter</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      temporary
      fixed
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          active-class="text--accent-4"
        >
          <v-list-item to="/">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <v-list-item to="/about">
            <v-list-item-icon>
              <v-icon>mdi-human-greeting</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About</v-list-item-title>
          </v-list-item>
          <v-list-item to="/works">
            <v-list-item-icon>
              <v-icon>mdi-cellphone-link</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Works</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      flat
      tile
      class="text-center"
    >
      <v-card-text>
        &copy; {{ new Date().getFullYear() }} — <strong>Keisuke Ishigami / 石上 敬祐</strong>
      </v-card-text>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
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
