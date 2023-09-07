<template>
  <div class="carousel-container">
    <vue-slick-carousel v-bind="settings">

      <div class="carousel-item">
        <h1>DIGIVICE Api</h1>
        <a  href="https://yeyref.github.io/digimonYR/" target="_blank" rel="noopener noreferrer">
          <img src="img/Screenshot_digimonjpeg.jpg" alt="Imagen 1" />
        </a>
        <p>Consumo de api externa de <a class="efecto" href="https://digimon-api.vercel.app/" target="_blank"
            rel="noopener noreferrer">digimon</a> mediante petición get y renderizado.</p>
        <ul>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>Bootstrap</li>
          <li>Fetch</li>
        </ul>
      </div>

      <div class="carousel-item">
        <h1>Games Opinion</h1>
        <a href="https://github.com/Yeyref/drilling_mod_6" target="_blank" rel="noopener noreferrer">
          <img src="img/Captura de pantalla 2023-09-02 181447.png" alt="Imagen 2" />
        </a>

        <p>Proyecto donde puedes comentar, editar y eliminar opiniones despues de dar click a cualquier juego
          mostrado en el viewport, consume la api de <a class="efecto" href="https://rawg.io/apidocs" target="_blank"
            rel="noopener noreferrer">RAWG</a>,
          puedes dar me gusta y darle una cierta cantidad de coins al juego seleccionado.</p>
        <ul class="is-flex-wrap-wrap">
          <li>VueJS</li>
          <li>Bootstrap-Vue</li>
          <li>Axios</li>
        </ul>
      </div>

      <div class="carousel-item">
        <h1>Stars Wars API</h1>
        <a href="https://github.com/Yeyref/drillingFinalMod5" target="_blank" rel="noopener noreferrer">
          <img src="img/Captura de pantalla 2023-08-31 181326.png" alt="Imagen 3" />
        </a>

        <p>¿Alguna vez has querido saber cómo serían los personajes de ficción en la vida real? En este proyecto los
          usuarios tienen una mejor idea de cómo serían algunos de
          sus personajes favoritos de Star Wars, en la vida real.</p>
        <ul class="is-flex-wrap-wrap">
          <li>JavaScript</li>
          <li>HTML5</li>
          <li>Bootstrap</li>
          <li>CSS3</li>
        </ul>

      </div>

      <div class="carousel-item">
        <h1>Festival de ROCK Y EDM</h1>
        <a href="https://yeyref.github.io/FestivalMusica_inicio/" target="_blank" rel="noopener noreferrer">
          <img src="img/Screenshot_rockjpeg.jpg" alt="Imagen 4" />
        </a>
        <p>Pagina main de festival de musica, donde se separa por secciones que incluye line up, precio de tickets y
          galeria de fotos.</p>
        <ul class="is-flex-wrap-wrap">
          <li>JavaScript</li>
          <li>HTML5</li>
          <li>SASS</li>
          <li>CSS3</li>
        </ul>
      </div>

    </vue-slick-carousel>
    <div class="container">
      <p class="has-text-centered" style=" margin-top:3rem;">Inspirado por la web, diseños y otros pensamientos que surgieron en alguna madrugada, Hecho con VueJS 2.0 & BULMACSS © <br> {{ this.fecha }} </p>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';

export default {
  name: 'CarouselComponent',
  data() {
    return {
      fecha: '',
      settings: {
        "autoplay": true,
        "dots": false,
        "infinite": true,
        "initialSlide": 1,
        "speed": 100,
        "slidesToShow": 1,
        "slidesToScroll": 1,
        "swipeToSlide": true
      }
    }
  },
  components: {
    VueSlickCarousel,
  },
    mounted() {
    this.obtenerFechaActual();
  },
    methods: {
        obtenerFechaActual() {
      const fecha = new Date();
      const dia = fecha.getDate();
      const mes = fecha.getMonth() + 1; 
      const año = fecha.getFullYear();

      this.fecha = `${dia}/${mes}/${año}`;
    }
}
}
</script>

<style scoped>
.carousel-container {
  display: flex;
  align-items: center;
  flex-direction: column;
 
}

.carousel-item{
  padding:0 1rem;
}

.slick-slider {
  display: flex;
  flex-direction: row;
  align-items: center;
 max-width: 35rem;
}

@media (max-width: 530px ){ 
    .slick-slider{
      display: grid;
      max-width: 20rem;
    }
}

.efecto{
  color: rgb(226, 232, 240, 1)
}

.efecto:hover {
  transition: 0.2s;
  filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));
}

img {
  border-radius: 10px;
}
img:hover{
  transform: scale(1.01);
  transition: 0.7s;
}

h1 {
  text-align: center;
  color: rgb(226, 232, 240, 1);
  line-height: 50px;
  margin: 3px;
}

ul {
  margin:0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: baseline;
  list-style: none;
}

li {
  background-color: rgba(45, 212, 191, .1);
  color: rgb(94, 234, 212, 1);
  border-radius: 9999px;
  padding: 0.25rem 0.75rem;
}

p {
  margin-top: 5px;
}

::v-deep .slick-arrow:before {
  color: #2f3241;
  opacity: 1;
}
</style>