<template>
  <div id="app">
    <!-- Cabecera -->

    <cabecera></cabecera>

    <!-- Banner -->
    <banner-principal></banner-principal>

    <!-- --------------- Sección de Servicios ---------------  -->
    <seccion-servicios></seccion-servicios>

    <!-- --------------- Sección de Noticias ---------------  -->
    <section class="noticias" id="noticias">
        <div class="tituloNews">

            <h2> <span>N</span>oticias</h2>
            <p>Enterate de lo último en tecnología del mundo en este portal</p>

        </div>
        
           <seccion-noticias></seccion-noticias> 

        
    </section>
    
    
    <!-- --------------- Sección de Equipo ---------------  -->
    <section class="equipo" id="equipo">
    <div class="tituloTeams">

        <h2> <span>N</span>uestro <span>E</span>quipo</h2>
        <p>Tienes el mejor personal a tu disposición</p>

    </div>
  <team-card></team-card>

    
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
  }
}
</script>

