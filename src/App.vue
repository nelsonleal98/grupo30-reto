<template>
  <div id="app">
    
   
    <!-- --------------- Sección de Servicios ---------------  -->
    <seccion-servicios></seccion-servicios>

    <!-- --------------- Sección de Noticias ---------------  -->
    <div class="noticias" id="noticias">
        <div class="tituloNews">

            <h2> <span>N</span>oticias</h2>
            <p>Enterate de lo último de tecnología en el mundo en este portal</p>

        </div>
        
           <seccion-noticias></seccion-noticias> 

        
    </div>
    
    
    <!-- --------------- Sección de Equipo ---------------  -->
    <div class="equipo" id="equipo">
        <div class="tituloTeams">
            <h2> <span>N</span>uestro <span>E</span>quipo</h2>
            <p>Tienes el mejor personal a tu disposición</p>                 
        </div>
        <div class="integrantes">
          <div v-for="(miembro, index) of Equipo" :key="index">
                <team-card :member="miembro"></team-card>
              </div>
        </div>   
    </div>
<!-- --------------- Sección Footer ---------------  -->
  <seccion-footer></seccion-footer>
    
  </div>
  
</template>


<script>
import SeccionServicios from './components/SeccionServicios.vue'
import SeccionNoticias from './components/SeccionNoticias.vue'
import TeamCard from './components/TeamCard.vue'
import SeccionFooter from './components/SeccionFooter.vue'


export default {
  name: 'App',
  components:{
    SeccionServicios,
    SeccionNoticias,
    TeamCard,
    SeccionFooter,
  },
  data(){
    return{
      Equipo:[
        {
          codigo:1,
          nombre:'Nelson Leal',
          descripcion: 'Ingeniero en Telecomunicaciones egresado de la Universidad de Pamplona, con conocimiento en redes, programación e infrastructura soporte bajo RITEL. Originario de la ciudad de Cúcuta',
          rol:'Arquitecto de Software',
          imagen:"./images/Nelson.png"
        },
        {
          codigo:2,
          nombre:'Luis Monsalve',
          descripcion: 'Lic. en Matemáticas egresado de la Universidad Industrial de Santander. Experto en la enseñanza de aplicaciones en matemáticas y estadística. Originario de la ciudad de Barranquilla.',
          rol:'Desarrollador Frontend',
          imagen:"./images/Luis.png"
        },
        {
          codigo:3,
          nombre:'Daniel Hermosilla',
          descripcion: 'Estudiante de Ingeniería de Sistemas de la Universidad de Cundinamarca con conocimiento en desarrollo de videojuegos y web. Originario de la ciudad de Zipaquirá',
          rol:'Tester',
          imagen:"./images/Daniel.png"
        },
        {
          codigo:4,
          nombre:'Miguel Sandoval',
          descripcion: 'Ingeniero de sistemas, conocimientos en educación y desarrollo del pensamiento computacional. Originario de la ciudad de Bogotá',
          rol:'Analista de Software',
          imagen:"./images/Miguel.png"
        },
        {
          codigo:5,
          nombre:'Luisa Pedraza',
          descripcion: 'Ingeniera Electrónica egresada de la Universidad Incca de Colombia, con conocimientos en el área de control y automatización. Originaria de la ciudad de Bogotá',
          rol:'Desarrollador Backend',
          imagen:"./images/Luisa.png"
        }
      ]
    }
  }
}
</script>

