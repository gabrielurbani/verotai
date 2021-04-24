<template>
  <v-container class="d-flex flex-wrap">  
    <v-row>
      <v-col
        sm="10"
        offset-sm="1"
        lg="5"
        v-for="card in cards" 
        :key="card.id" 
      >
        <v-card 
          class="rounded-l mx-auto my-8 pa-4"
          :color=" `${card.backgroundColor}`"
          max-width="600"
          elevation="3"
        >
        <v-img
          :src="card.img"
          height="350px"
        ></v-img>
        <v-card-title class="white" >
           {{ card.title }}
        <v-divider  inset role="presentation"></v-divider>
        </v-card-title>
        <v-card-text class="white">
          {{ card.description }}
        </v-card-text>
        <v-card-actions class="white">
        <v-spacer></v-spacer>
        <v-btn
          small
          :color="`${card.color}`"
          class="white--text"
        >
        <v-icon>mdi-plus</v-icon>
        Me interesa
      </v-btn>
    </v-card-actions>
  </v-card>
  </v-col>
</v-row>
  </v-container>
</template>
<script>
export default {
  props: ["id"],
  data: () => {
    return {
      cards: [
        {
          id: 0,
          title: ": Zen-Shiatzu",
          description: `El shiatsu es una de las más antiguas formas de curar con las manos, cuya base teórica es la milenaria medicina china. 
La palabra shiatsu significa en japonés "presión con los dedos", sin embargo las presiones se aplican con dedos, palmas, codos, rodillas y también pies. El shiatsu acttúa sobre el movimiento de la energía, conocida con el nombre de  ki o chi que circula en el cuerpo por trayectos definidos: los meridianos. El terapeuta aplica diferentes grados de presión sobre los meridianos y zonas específicas del cuerpo para equilibrar la energía de todo el organismo. Beneficios: fomenta el equilibrio físico y enérgetico, calma todo tipo de dolores, ayuda en casos de insomnio, combate el stress, armoniza y otorga un profundo bienestar.`,
          img: require("@/assets/zen-shiatzu.jpg"),
          color: "green lighten-2",
          backgroundColor: "#C8E3D0",
          open: false
        },
        {
          id: 1,
          title: ": Masaje Thailandes",
          description: `El nuad bo rarn o masaje tradicional tailandés, se practica desde hace mas de 2500 años. La palabra nuad significa "tocar con la intención de aliviar o sanar", mientras que bo rarn significa "todo aquello que es antiguo, sagrado y reverenciado". 
El propósito del masaje tailandés es el de solucionar los problemas que se manifiestan a nivel físico, mental y emocional, además de activar los mecanismos de auto curación del cuerpo, logrando armonía y equilibrio en la persona que lo recibe. 
Se utilizan técnicas de presión; con palma, pulgar, rodilla, codos 
y pies. También distintos estiramientos que evocan a las posturas de yoga. Es ideal para aliviar tensiones, liberar contracturas, incrementar la flexibilidad, lograr una profunda relajación y olvidarse del stress.	`,
          img: require("@/assets/masaje-tailandes.jpg"),
          color: "yellow lighten-1",
          backgroundColor: "#F4FEA4",
          open: false
        },
        {
          id: 2,
          title: ": Polaridad",
          description: `Randolf Stone, creador de la terapia de polaridad, integró sus conocimientos occidentales y orientales (osteopatía, naturoterapia, quiropráctica, acupuntura, herbología, ayurveda) que le proporcionaron el conocimiento de los campos electromagneticos sutiles del cuerpo. La terapia de la polaridad, centra su atención en el estudio de la " fuerza de vida", nuestro campo energético y su relación con el universo. Su base es la simetría, la unión de los opuestos y el equilibrio entre antagónicos y contrarios, para lograr la unidad mente, cuerpo y alma. En la práctica se utilizan técnicas de contacto física y no físico para enviar energía a todo el sistema, abrir los puntos bloqueados, alineando la fuerza de vida en el cuerpo. Como resultado se vivencia una profunda relajación, paz mental, equilibrio, energético del cuerpo.`,
          img: require("@/assets/polaridad.jpg"),
          color: "cyan",
          backgroundColor: "#AAE0E6",
          open: false
        },
        {
          id: 3,
          title: ": Cuencos Tibetanos",
          description: `Los cuencos tibetanos son instrumentos sagrados y antiguos provenientes de nepal. El sonido de los cuencos tibetanos y sus  armónicos, sirven para equilibrar los planos físico, mental y emocional. Los sonidos y las vibraciones que generan los cuencos, tienen la propiedad de modificar las ondas cerebrales, favoreciendo los estados de relajación y meditación. El masaje sonoro implica hacer sonar el cuenco muy cerca del cuerpo o  bien apoyado en el cuerpo para que llegue tanto el sonido como la vibración, que nos afecta por el principio de resonancia. Dentro de los mas importantes beneficios encontramos: el logro de una profunda relajación y armonización, alivio del stress, equilibrio de los hemisferios cerebrales, la mejora en la concentración, armonización del sistema nervioso y un refuerzo de las defensas del organismo. "Una experiencia única"`,
          img: require("@/assets/cuenco.jpg"),
          color: "deep-purple lighten-2",
          backgroundColor: "#DED5E6",
          open: false
        },
        {
          id: 4,
          title: ": Reflexología",
          description: `La reflexología es una terapia que aspira a promover el restablecimiento del equilibrio energético del organismo. Se trabaja en los pies y en las manos, estimulando las áreas reflejas de los órganos del cuerpo. Entre sus beneficios: alivia tensiones musculares generales, alivia el stress, mejora las funciones del sistema nervioso, circulatorio y digestivo, contribuye a la eliminación de toxinas. Mejora tambien los desequilibrios emocionales y el estado de ánimo. Estimula el poder curativo latente en el cuerpo.`,
          img: require("@/assets/reflexologia.jpg"),
          color: "deep-orange lighten-2",
          backgroundColor: "#F6DFB1",
          open: false
        },
        {
          id: 5,
          title: ": Shantala",
          description: `Shantala o masaje para bebés "es un arte tan antiguo como profundo". Se origina en India en donde las mamás le dan masaje a sus bebés cotidianamente, profundizando a través del masaje los lazos afectivos, relajando su cuerpito para un buen desarrollo del organismo. Los beneficios son muchos y en varios niveles: estimula el sistema circulatorio, gastrointestinal, inmunológico y respiratorio. Logra liberar el cuerpo de angustias, lo relaja y ayuda también en la coordinación muscular. Emocionalmente, la estimulación táctil (primer sentido en desarrollarse) es un medio de comunicación, de expresión de cariño. 
La propuesta es brindar el conocimiento del shantala a los padres que deseen incorporar esta práctica saludable y de amor en la vida cotidiana con sus bebés `,
          img: require("@/assets/shantala.jpg"),
          color: "purple lighten-3",
          backgroundColor: "#F6E2E7",
          open: false
        },
        {
          id: 6,
          title: ": Ayurveda",
          description: `El ayuveda es un sistema holístico de medicina originario de la India. La palabra ayurveda significa, en sánscrito: "ciencia de la vida". Se trata de un sistema de curación practicado desde hace mas de 5000 años. En el ayurveda el masaje es un arte muy desarrollado. Se trabaja sobre los puntos marmas, o centros energéticos logrando movilizar la energía y beneficiando así a todo el organismo. Se utilizan aceites esenciales y con movimientos específicos se apunta al balance de las energías internas de cada persona en particular (biotipos: vata, pitta, kapha). El masaje aumenta la circulación y remueve los desechos de los tejidos mejorando la nutrición de estos. Es además muy relajante, ayuda a superar momentos de fatiga, stress, depresión. Tonifica los tejidos nerviosos y musculares y ayuda a eliminar toxinas. Es un verdadero reencuentro con el bienestar general.`,
          img: require("@/assets/ayurveda.jpg"),
          color: "red lighten-1",
          backgroundColor: "#BA5A59",
          open: false
        }
      ]
    };
  }
};
</script>

<style>
.v-application  {
    font-family: 'Playfair Display', serif;
}
</style>