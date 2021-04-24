<template>
  <v-container>
      <v-row>
          <v-col>
              <v-card id="about" 
               class="d-flex flex-column rounded-l mx-auto my-8 pa-2"
               max-width="1200"
               elevation="3">
                 <v-img 
                 class="white mt-5 rounded-circle" 
                 width="100%" 
                 max-width="300"
                 src="../assets/veroroisinblit.jpg">
                 </v-img>
                 <v-img src="../assets/verotai.png"
                 class="white"
                 ></v-img>  
<v-icon class="mt-n2"
color="orange lighten-1">
            mdi-circle
          </v-icon>
                  <v-divider class="mx-4"></v-divider>
                  <v-card-text class="white"
                 >
                      <span>"Desde 1991 me dedico al estudio y profundización del ser humano, y a la integración del mismo en mente, cuerpo, espíritu como totalidad en sus múltiples manifestaciones, con el fin de aportar un reestablecimiento de la armonía, bienestar mejorando así la calidad de vida". 

Durante mi constante formación he obtenido los 
siguientes títulos y certificados: 

- Profesora Nacional Superior de Expresión Corporal 
- (Escuela Nacional de danzas "María Ruanova") 
- Profesora de hatha yoga (Instituto I.P.E.F.)
- Masaje chino An-mo (Facultad de Medicina de Bs As) 
- Terapeuta de Shiatsu (Esc. de Valerie Gaillare) 
- Terapeuta de Zen shiatsu (Centro Brillo del sol)
- Terapeuta de Masaje Tradicional Tailandés (Centro Brillo del Sol) 
- Terapia de la Polaridad (Esc. de Masajes Tradicionales) 
- Masaje Vibracional con Cuencos Tibetanos (E. de Masaje Tradicional) 
- Sanación en el agua "Aqua Healing" 
- (Prof. Marcel Breedveld) 
- Reiki Jin Kei do (Profesor Jorge Martin )
- Masajes Ayurveda (Centro Argentino de Ayurveda 
- “Dr Domar Singh Madoriya”)</span>
                  </v-card-text>
              </v-card>
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {
name: "About"
}
</script>

<style>
.v-application h1, span {
    font-family: 'Playfair Display', serif;
}
</style>