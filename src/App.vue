<template>
  <div id="app">
    <!-- Cabecera -->

    <cabecera></cabecera>

    <!-- Banner -->
    <banner-principal></banner-principal>

    <div class="container-slider">
      <link rel="stylesheet" href="cssslider_files/csss_engine1/style.css">
      <div class='csslider1 autoplay '>
        <input name="cs_anchor1" id='cs_slide1_0' type="radio" class='cs_anchor slide' >
        <input name="cs_anchor1" id='cs_slide1_1' type="radio" class='cs_anchor slide' >
        <input name="cs_anchor1" id='cs_slide1_2' type="radio" class='cs_anchor slide' >
        <input name="cs_anchor1" id='cs_play1' type="radio" class='cs_anchor' checked>
        <input name="cs_anchor1" id='cs_pause1_0' type="radio" class='cs_anchor pause'>
        <input name="cs_anchor1" id='cs_pause1_1' type="radio" class='cs_anchor pause'>
        <input name="cs_anchor1" id='cs_pause1_2' type="radio" class='cs_anchor pause'>
        <ul>
          <li class="cs_skeleton"><img src="/images/smartphone.png" style="width: 100%;"></li>
          <li class='num0 img slide'> <img src='/images/smartphone.png' alt='' title='' /></li>
          <li class='num1 img slide'> <img src='/images/camara.jpg' alt='' title='' /></li>
          <li class='num2 img slide'> <img src='/images/smartwatch.jpg' alt='' title='' /></li>
        </ul>
        <div class='cs_description'>
          <label class='num0'></label>
          <label class='num1'></label>
          <label class='num2'></label>
        </div>
        <div class='cs_play_pause'>
          <label class='cs_play' for='cs_play1'><span><i></i><b></b></span></label>
          <label class='cs_pause num0' for='cs_pause1_0'><span><i></i><b></b></span></label>
          <label class='cs_pause num1' for='cs_pause1_1'><span><i></i><b></b></span></label>
          <label class='cs_pause num2' for='cs_pause1_2'><span><i></i><b></b></span></label>
          </div>
        <div class='cs_arrowprev'>
          <label class='num0' for='cs_slide1_0'><span><i></i><b></b></span></label>
          <label class='num1' for='cs_slide1_1'><span><i></i><b></b></span></label>
          <label class='num2' for='cs_slide1_2'><span><i></i><b></b></span></label>
        </div>
        <div class='cs_arrownext'>
          <label class='num0' for='cs_slide1_0'><span><i></i><b></b></span></label>
          <label class='num1' for='cs_slide1_1'><span><i></i><b></b></span></label>
          <label class='num2' for='cs_slide1_2'><span><i></i><b></b></span></label>
        </div>
        <div class='cs_bullets'>
          <label class='num0' for='cs_slide1_0'> <span class='cs_point'></span>
            <span class='cs_thumb'><img src='cssslider_files/csss_tooltips1/smartphone.png' alt='' title='' /></span></label>
          <label class='num1' for='cs_slide1_1'> <span class='cs_point'></span>
            <span class='cs_thumb'><img src='cssslider_files/csss_tooltips1/camara.jpg' alt='' title='' /></span></label>
          <label class='num2' for='cs_slide1_2'> <span class='cs_point'></span>
            <span class='cs_thumb'><img src='cssslider_files/csss_tooltips1/smartwatch.jpg' alt='' title='' /></span></label>
        </div>
      </div>
    </div>
    <!-- --------------- Sección de Servicios ---------------  -->
    <seccion-servicios></seccion-servicios>

    <!-- --------------- Sección de Noticias ---------------  -->
    <section class="noticias" id="noticias">
        <div class="tituloNews">

            <h2> <span>N</span>oticias</h2>
            <p>Enterate de lo último de tecnología en el mundo en este portal</p>

        </div>
        
           <seccion-noticias></seccion-noticias> 

        
    </section>
    
    
    <!-- --------------- Sección de Equipo ---------------  -->
    <section class="equipo" id="equipo">
        <div class="tituloTeams">
            <h2> <span>N</span>uestro <span>E</span>quipo</h2>
            <p>Tienes el mejor personal a tu disposición</p>                 
        </div>
        <div class="integrantes">
          <div v-for="(miembro, index) of Equipo" :key="index">
                <team-card :member="miembro"></team-card>
              </div>
        </div>   
    </section>
<!-- --------------- Sección Footer ---------------  -->
  <seccion-footer></seccion-footer>
    
  </div>
</template>

<script>
import BannerPrincipal from './components/BannerPrincipal.vue'
import Cabecera from './components/Cabecera.vue'
import SeccionServicios from './components/SeccionServicios.vue'
import SeccionNoticias from './components/SeccionNoticias.vue'
import TeamCard from './components/TeamCard.vue'
import SeccionFooter from './components/SeccionFooter.vue'


export default {
  name: 'App',
  components:{
    Cabecera,
    BannerPrincipal,
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

