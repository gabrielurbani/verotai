<template>
  <v-container>
      <v-col
          sm="10"
    offset-sm="1"
    lg="4"
    offset-lg="1"
> <v-row>
          <v-card 
              :width="width" 
              class="d-flex flex-column rounded-xl mx-auto my-8 pa-2"
               color="#fece00"
               elevation="10"
             >
              <v-img width=100%
              max-width="250px"
              src="../assets/mandalita.png">

              </v-img>
              <v-card-title 
              class="white orange--text" 
              
              ><h1>verotai</h1></v-card-title>
          </v-card>
      </v-row></v-col>
  </v-container>
</template>

<script>
export default {
name: "Verotai",
computed: {
      width () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 220
          case 'sm': return 400
          case 'md': return 500
          case 'lg': return 600
          case 'xl': return 800
        }
      },
    },
}


</script>

<style>
.v-application h1 {
    font-family: 'Playfair Display', serif;
}
</style>