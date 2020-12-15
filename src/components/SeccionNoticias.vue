<template>
<div class="fourNews">
    <div class="box" v-for="(noticia, index) of noticias" :key="index">

                <div class="nombreNews">
                    <h3> <b>{{noticia.title}}</b> </h3>
                </div>

                <div class="imgNews">
                    <img :src="noticia.image" alt="Imagen noticia">
                </div>

                <div class="descripcionNews">
                    <p> {{noticia.description}} </p>
                </div>
                <div class="urlNoticia">
                    <a class="masNews" :href="noticia.url" target="_blank"> Ver Noticia</a>
                </div>

    </div>
</div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "SeccionNoticias",
        data(){
            return{
                noticias: null
            }
        },
        created(){
            axios
                .get('https://gnews.io/api/v4/top-headlines?topic=technology&max=4&lang=es&token=2f143a88cb0e581c59d2ba5e8b249c46')
                .then( response => {this.noticias = response.data.articles.slice(0,4)} )
            console.log(this.peliculas)
        }
    }
</script>
