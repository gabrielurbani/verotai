<template>
  <v-container>
      <v-row>
          <v-col>
              <v-card
  
    class="mx-auto my-1"
    max-width="900"
  >
  
    <v-img
      height="250"
      src="../assets/veotai_contacto.jpg"
    ></v-img>

    <v-card-title class="orange--text display-1" >: Contacto</v-card-title>

    <v-divider class="mx-5"></v-divider>
    <v-card-text>
      
      <div class="my-3 subtitle-1">
      <v-icon 
color="orange lighten-3">
            mdi-phone
          </v-icon>  4544 0290
      </div>

      <div class="my-3 subtitle-1">
      <v-icon 
color="orange lighten-3">
            mdi-whatsapp
          </v-icon>  11 4061 1849
      </div>
<div class="my-3 subtitle-1">
      <v-icon 
color="orange lighten-3">
            mdi-email
          </v-icon>  verdevero@yahoo.com
      </div>
      </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title class="justify-center">Veronica Roisinblit | Terapeuta</v-card-title>

  </v-card>
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {
name: "Contacto"
}
</script>

<style>
.v-application  {
    font-family: 'Playfair Display', serif;
}
#contacto{
    border: 2rem solid orange !important;
}
</style>