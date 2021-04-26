<template>
  <div>
    <v-app-bar>
<router-link to="/">       <v-img alt="Verotai logo"
    class="mx-2"
    src="../assets/mandala_icon.png"
    max-height="40"
    max-width="40"
    contain
    id="hithere"
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
  
              <v-btn href="https://www.facebook.com/verotaiterapeutaholistica/" target="_blank" text>
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
  
        <v-btn href="https://www.youtube.com/user/verotai1000" target="_blank" text>
          <v-icon>mdi-youtube</v-icon>
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
        { title: 'Instagram', link: 'https://www.instagram.com/la_verotai/', icon: 'mdi-instagram'},
        { title: 'Facebook', link: "https://www.facebook.com/verotaiterapeutaholistica/", icon: 'mdi-facebook' },
        { title: 'Youtube', link: 'https://www.youtube.com/user/verotai1000', icon: 'mdi-youtube'}
      ],
      servicio:[
        {title: ': Zen-Shiatzu', link: 'servicios.card.0'},
        {title: ': Masaje Thailandes', link: 'servicios.card.1'},
        {title: ': Polaridad', link: 'servicios.card.2'},
        {title: ': Cuencos tibetanos', link: 'servicios.card.3'},
        {title: ': Reflexologia', link: 'servicios.card.4'},
        {title: ': Shantala', link: 'servicios.card.5'},
        {title: ': Ayurveda', link: 'servicios.card.6'}

      ],
      closeOnContentClick: true,
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
#flash {
  animation: flash 1000ms ease 2s 3 alternate;
}
@keyframes flash {
	from { opacity: 1; }	
	to { opacity: 0; }
}
#hithere {
  animation: hithere 1s ease 2s 1;
}
@keyframes hithere {
  30% { transform: scale(1.2); }
  40%, 60% { transform: rotate(-20deg) scale(1.2); }
  50% { transform: rotate(20deg) scale(1.2); }
  70% { transform: rotate(0deg) scale(1.2); }
  100% { transform: scale(1); }
}

</style>