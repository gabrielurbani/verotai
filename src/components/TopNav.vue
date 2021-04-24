<template>
  <div>
    <v-app-bar>
<router-link to="/">       <v-img alt="Verotai logo"
    class="mx-2"
    src="../assets/mandala.png"
    max-height="40"
    max-width="40"
    contain
  ></v-img></router-link>
      <v-spacer></v-spacer>

      <!-- mobile menu button -->
      <span class="hidden-sm-and-up">
        <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </span>

      <!-- desktop & tablet menu -->
      <v-toolbar-items class="hidden-xs-only ">
        <v-btn class="text-capitalize font-weight-bold" to="Servicios" text>
          : Servicios
        </v-btn>
        <v-btn class="text-capitalize font-weight-bold" to="About" text>
          : Sobre Mi
        </v-btn>
        <v-btn class="text-capitalize font-weight-bold" to="Contacto" text>
          : Contacto
        </v-btn>
                    <v-btn href="https://www.instagram.com/la_verotai/" target="_blank" text>
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
  
              <v-btn href="https://www.facebook.com/verotai.terapiasholisticas" target="_blank" text>
          <v-icon>mdi-facebook</v-icon>
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
            <v-list-item-title><v-icon>{{item.icon}}</v-icon> {{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-divider class="mx-4"></v-divider>
      <v-list dense>
        <v-list-item
          v-for="item in social"
          :key="item.title"
          :href="item.link"
          link
        >

          <v-list-item-content>
            <v-list-item-title><v-icon>{{item.icon}}</v-icon> {{ item.title }}</v-list-item-title>
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
        { title: 'Home', link: '/', icon: 'mdi-home' },
        { title: 'Servicios', link: 'servicios', icon: 'mdi-meditation' },
        { title: 'Sobre Mi', link: 'about', icon: 'mdi-face-woman' },
        { title: 'Contacto', link: 'contacto', icon: 'mdi-mail' },
      ],
      social: [
        { title: 'Facebook', link: "https://www.facebook.com/verotai.terapiasholisticas", icon: 'mdi-facebook' },
        { title: 'Instagram', link: 'https://www.instagram.com/la_verotai/', icon: 'mdi-instagram'}
      ]
    }
  }
}
</script>
<style>

.v-application {
        
    font-family: 'Playfair Display', serif;
}
.v-toolbar__content{
  font-family: 'Playfair Display', serif;

}
.v-app-bar {
  background-color: #FAAC00; /* fallback color if gradients are not supported */
  background-image: -webkit-linear-gradient(75deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For Chrome 25 and Safari 6, iOS 6.1, Android 4.3 */
  background-image:    -moz-linear-gradient(75deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For Firefox (3.6 to 15) */
  background-image:      -o-linear-gradient(75deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For old Opera (11.1 to 12.0) */
  background-image:         linear-gradient(75deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* Standard syntax; must be last */
}
.v-navigation-drawer {
  background-color: #faac00; /* fallback color if gradients are not supported */
  background-image: -webkit-linear-gradient(290deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For Chrome 25 and Safari 6, iOS 6.1, Android 4.3 */
  background-image:    -moz-linear-gradient(290deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For Firefox (3.6 to 15) */
  background-image:      -o-linear-gradient(290deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* For old Opera (11.1 to 12.0) */
  background-image:         linear-gradient(290deg,hsl(64, 98%, 70%),hsl(41, 100%, 49%) ,hsl(41, 100%, 69%),hsl(64, 98%, 70%)); /* Standard syntax; must be last */
}
</style>