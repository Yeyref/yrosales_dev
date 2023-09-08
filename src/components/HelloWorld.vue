<template>
  <div class="content">
    <div class="container is-fluid ">
      <div>
        <nav class="navbar  is-transparent is-fixed-top" style="backdrop-filter: blur(10px);">
          <div class="navbar-brand">
            <a class="colorPrimary" href="#" style="display: flex; align-content: center; flex-wrap: wrap;">
              <p> YJRR<strong>|Front-End Development</strong></p>
            </a>
            <div class="navbar-burger has-text-light" data-target="navbarExampleTransparentExample">
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
                Formación
              </a>
              <a href="#proyectos" class="navbar-item">
                Proyectos
              </a>
            </div>
          </div>
        </nav>
      </div>

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
                        Formación
                      </a>
                      <a href="#proyectos" class="navbar-items">
                        Proyectos
                      </a>
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
              <div>
                <a href="pdf/CVYefersonJoseRosalesReyes.pdf" download="CVYefersonJoseRosalesReyes.pdf" target="_blank"
                  style="display: flex;
                        justify-content: center; 
                        padding-top: 2rem; 
                        text-transform: uppercase; 
                        color: rgb(226, 232, 240, 0.9); 
                        filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));"
                        >¡Descarga acá mi curriculum vitae para ver mas!</a>
              </div>
          </section>
          <section id="formacion">
            <EduInfoComponent></EduInfoComponent>
              <div>
                <a href="pdf/CVYefersonJoseRosalesReyes.pdf" download="CVYefersonJoseRosalesReyes.pdf" target="_blank"
                  style="display: flex;
                        justify-content: center; 
                        padding-top: 2rem; 
                        text-transform: uppercase; 
                        color: rgb(226, 232, 240, 0.9); 
                        filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));"
                        >¡Descarga acá mi curriculum vitae para ver mas!</a>
              </div>
          </section>
          <section id="proyectos">
            <ProyInfoComponent></ProyInfoComponent>
          </section>
        </main>
      </div>
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
    NameComponent,
    FirstInfoComponent,
    ExpInfoComponent,
    EduInfoComponent,
    ProyInfoComponent,
    IconSocialComponent
  },
  mounted() {
    const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);
    $navbarBurgers.forEach(el => {
      el.addEventListener('click', () => {
        const target = el.dataset.target;
        const $target = document.getElementById(target);
        el.classList.toggle('is-active');
        $target.classList.toggle('is-active');
      });
    });
  },
};

</script>

<style scoped>
@media (min-width: 1024px) {
  header {
    position: fixed;
  }

  section {
    min-height: 100vh;
    padding-top: 100px;
  }

  .navbar-vertical {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 1rem;
    gap: 1rem;
  }

  .menu-small {
    display: none;
  }
}

@media (min-width: 1124px) {
  .centrado {
    margin-left: 5rem;
  }
}

nav {
  height: 90px;
  padding: 16px;
}

@media (max-width: 1023px) {
  section {
    min-height: 50vh;
    padding-top: 10rem;
  }
}

#acerca {
  padding-top: 6rem;
  scroll-margin-top: 6rem;
}

.navbar {
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

a {
  color: rgb(148, 163, 184, 1);
  transition: 0.2s;
  background-color: transparent;
}

.colorPrimary {
  color: rgb(226, 232, 240, 0.9)
}

.navbar-items:hover {
  background-color: transparent;
  transform: scale(1.2);
  text-decoration: underline;
  transition: 0.2s;
  color: rgb(226, 232, 240, 1);
  filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));
}

.align-menu {
  margin-top: 20px;
  justify-content: center;
}
</style>
