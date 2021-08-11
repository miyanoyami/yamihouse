<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>
        <router-link to="/" class="toolbar-title" style="color:inherit; text-decoration: none;">
          Miyano Yami
        </router-link>
      </v-toolbar-title>
      <v-spacer />
      <v-btn
        icon
        href="https://twitter.com/miyanoyami83"
        target="_blank"
      >
        <v-icon>mdi-twitter</v-icon>
      </v-btn>
      <v-btn
        icon
        href="https://www.youtube.com/c/miyanoyami"
        target="_blank"
      >
        <v-icon>mdi-youtube</v-icon>
      </v-btn>
      <v-btn
        icon
        href="https://github.com/miyanoyami"
        target="_blank"
      >
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; 2021 Miyano Yami</span>
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
          title: 'Top',
          to: '/'
        },
        {
          icon: 'mdi-account-circle',
          title: 'Profile',
          to: '/profile'
        },
        {
          icon: 'mdi-wrench',
          title: 'System',
          to: '/system'
        },
        {
          icon: 'mdi-gamepad-square',
          title: 'Game',
          to: '/game'
        },
        {
          icon: 'mdi-star-outline',
          title: 'Skill',
          to: '/skill'
        },
        {
          icon: 'mdi-bank',
          title: 'Gallery',
          to: '/gallery'
        }
      ],
      miniVariant: false,
      rightDrawer: false
    }
  }
}
</script>

<style scoped>
.v-application {
  background-color: #fffbfb
}
</style>
