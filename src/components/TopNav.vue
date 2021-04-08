<template>
  <div>
    <v-app-bar color="#FFC600">
       <v-img alt="Verotai logo"
    class="mx-2"
    src="../assets/mandala.png"
    max-height="40"
    max-width="40"
    contain
  ></v-img>
      

      <v-spacer></v-spacer>

      <!-- mobile menu button -->
      <span class="hidden-sm-and-up">
        <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </span>

      <!-- desktop & tablet menu -->
      <v-toolbar-items class="hidden-xs-only">
        <v-btn to="/" text>
          Home
        </v-btn>
        <v-btn to="Servicios" text>
          Servicios
        </v-btn>
        <v-btn to="About" text>
          Sobre Mi
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer
      app
      v-model="drawer"
      class="orange lighten-1"
      fixed
      temporary
      right
      
    >
      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.link"
          link
        >

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: 'Home', link: '/', icon: 'home' },
        { title: 'Servicios', link: 'servicios', icon: 'servicio' },
        { title: 'Sobre Mi', link: 'about', icon: 'about' }
      ]
    }
  }
}
</script>