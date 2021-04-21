<template>
  <div>
    <v-app-bar>
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
<style>

.v-application {
        
    font-family: 'Playfair Display', serif;
}
.v-application v-btn{
  font-family: 'Playfair Display', serif;

}
.v-app-bar {
  background-color: #F07575; /* fallback color if gradients are not supported */
  background-image: -webkit-linear-gradient(left, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For Chrome 25 and Safari 6, iOS 6.1, Android 4.3 */
  background-image:    -moz-linear-gradient(left, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For Firefox (3.6 to 15) */
  background-image:      -o-linear-gradient(left, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For old Opera (11.1 to 12.0) */
  background-image:         linear-gradient(to left,#FAAC00, hsl(64, 98%, 70%), #FAAC00); /* Standard syntax; must be last */
}
.v-navigation-drawer {
  background-color: #F07575; /* fallback color if gradients are not supported */
  background-image: -webkit-linear-gradient(top, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For Chrome 25 and Safari 6, iOS 6.1, Android 4.3 */
  background-image:    -moz-linear-gradient(top, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For Firefox (3.6 to 15) */
  background-image:      -o-linear-gradient(top, #FAAC00, hsl(64, 98%, 70%), #FAAC00); /* For old Opera (11.1 to 12.0) */
  background-image:         linear-gradient(to bottom,#FAAC00, hsl(64, 98%, 70%), #FAAC00); /* Standard syntax; must be last */
}
</style>