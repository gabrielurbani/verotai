  <template>
  <v-container>
  <v-row>   
     <v-col> 
          <v-card 
              class="d-flex flex-column white rounded-l mx-auto my-8 pa-2  "
               color="#fece00"
               align-item="center"
               justify-center
               elevation="3"
               max-width="1200px"
             >
              <v-img
                class="white" 
                width="100%" 
                max-width="250"
                src="../assets/mandala.png"
              ></v-img>
              <v-img  
                class="justify-center" 
                src="../assets/verotai.png"
              ></v-img>              
              <v-icon 
                class="mt-n5"
                color="orange lighten-1">
              mdi-circle
              </v-icon>
              <v-card-subtitle class="text-xl-h4 mt-3 align-baseline" 
              >VERONICA ROISINBLIT | TERAPEUTA</v-card-subtitle>
          </v-card>
      </v-col></v-row>
  </v-container>
</template>
<script>
export default {
name: "Verotai",
}
</script>
<style>
.v-application h1 {
    font-family: 'Playfair Display', serif;
}
.v-card{
  align-items: center;
}
</style>