<template>
  <div class="content">

    <div class="container is-fluid ">
      <!-- Hero head: will stick at the top -->
    <div>
      <nav class="navbar  is-transparent is-fixed-top" style="backdrop-filter: blur(10px);">
        <div class="navbar-brand">
          <a class="colorPrimary" href="">
            YJRR<strong>|Front-End Development</strong>
        </a>
          <div class="navbar-burger" data-target="navbarExampleTransparentExample">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
            <div id="navbarExampleTransparentExample" class="navbar-menu align-menu menu-small">
              <div class="navbar is-transparent">
                <a href="#acerca" class="navbar-item is active">
                  Acerca de mi
                </a>
                <a href="#experiencia" class="navbar-item">
                  Experiencia
                </a>
                <a href="#formacion" class="navbar-item">
                  Formacion
                </a>
                <a href="#proyectos" class="navbar-item">
                  Proyectos
                </a>
                
              </div>
        </div>

      </nav>
      <!-- <navbar class="navbar">
          <div class="container ">
            <div class="navbar-brand  is-primary">
              <a class="navbar-item">
                YJRR<strong>|Front-End Development</strong>
              </a>
            </div>
          </div>
        </navbar> -->
    </div>


    

    <!-- Hero content: will be in the middle -->
    
      <div class=" columns is-desktop">
        <div class="column pt-6 mt-1 ">
          <header class="centrado">
            <div>
              <NameComponent></NameComponent>
            </div>
            <div id="navbarMenuHeroC" class="navbar-menu align-menu">
              <div class="navbar navbar-vertical">
                <a href="#acerca" class="navbar-items is active">
                  Acerca de mi
                </a>
                <a href="#experiencia" class="navbar-items">
                  Experiencia
                </a>
                <a href="#formacion" class="navbar-items">
                  Formacion
                </a>
                <a href="#proyectos" class="navbar-items">
                  Proyectos
                </a>
                <!-- <span class="navbar-item">
                                    <a class="button is-success is-inverted">
                                        <span class="icon">
                                            <i class="fab fa-github"></i>
                                        </span>
                                        <span>Download</span>
                                    </a>
                                </span> -->
              </div>

              
            </div>
              <div>
                <IconSocialComponent></IconSocialComponent>
              </div>

          </header>
        </div>


        <main class="column">
          <section id="acerca">
            <FirstInfoComponent></FirstInfoComponent>
          </section>
          <section id="experiencia">
            <ExpInfoComponent></ExpInfoComponent>
          </section>
          <section id="formacion">
            <EduInfoComponent></EduInfoComponent>
          </section>
          <section id="proyectos">
            <ProyInfoComponent></ProyInfoComponent>
          </section>
        </main>
      </div>

    

    <!-- Hero footer: will stick at the bottom -->
   <!--  <div class="hero-foot">
                <nav class=" is-boxed is-fullwidth">
                    <div class="container">
                      <h4 class="has-text-centered">Hecho con VueJS 2.0 Y BULMACSS </h4>
                       
                    </div> 
                  </nav>
                   
                
            </div>-->
            

  </div>
    </div>

    
</template>

<script>
import NameComponent from '@/components/NameComponent.vue';
import FirstInfoComponent from '@/components/FirstInfoComponent.vue';
import ExpInfoComponent from '@/components/ExpInfoComponent.vue';
import EduInfoComponent from '@/components/EduInfoComponent.vue';
import ProyInfoComponent from '@/components/ProyInfoComponent.vue';
import IconSocialComponent from '@/components/IconSocialComponent.vue';

export default {
  name: 'HomeView',
  components: {
    // HelloWorld,
    NameComponent,
    FirstInfoComponent,
    ExpInfoComponent,
    EduInfoComponent,
    ProyInfoComponent,
    IconSocialComponent
},
mounted() {
    // Get all "navbar-burger" elements
    const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

    // Add a click event on each of them
    $navbarBurgers.forEach(el => {
      el.addEventListener('click', () => {
        // Get the target from the "data-target" attribute
        const target = el.dataset.target;
        const $target = document.getElementById(target);

        // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
        el.classList.toggle('is-active');
        $target.classList.toggle('is-active');
      });
    });
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

@media (min-width: 1024px){ 
    header {
  position: fixed;
}
section{
    min-height: 100vh;
    padding-top: 100px;
}
.navbar-vertical{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 1rem;
  gap: 1rem;
}

.menu-small{
  display:none;
}
}


@media (min-width: 1124px){ 
  .centrado {
  margin-left: 5rem;
}
}

nav{
  height: 90px;
  padding: 16px;
}

@media (max-width: 1023px ){ 
    section{
    min-height: 70vh;
    padding-top: 13rem;
}
}



#acerca{
  padding-top: 6rem;
  scroll-margin-top: 6rem;
}
/* @media (min-width: 1024px){ 
    .navbar-vertical{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 1rem;
  gap: 1rem;
}
} */

.navbar{
  background-color: transparent;
}

.centrado {
  margin-top: 70px;
}

h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a{
  color: rgb(148, 163, 184, 1);
  transition: 0.2s;
  background-color: transparent;
}

.colorPrimary{
  color: rgb(226, 232, 240, 0.9)
}

.navbar-items:hover{
 background-color: transparent;
 transform: scale(1.2);
 text-decoration: underline;
  transition: 0.2s;
  color:rgb(226, 232, 240, 1) ;
  filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));
}

.align-menu{
  margin-top: 20px;
  justify-content: center;
}
</style>
