<template>
  <div>
    <a href="https://github.com/Yeyref" target="_blank" rel="noopener noreferrer">
      <font-awesome-icon class="icons" icon="fa-brands fa-github" size="2xl" />
    </a>
    <a href="https://www.linkedin.com/in/yeferson-rosales-4a37aa15a/" target="_blank" rel="noopener noreferrer">
      <font-awesome-icon class="icons" icon="fa-brands fa-linkedin" size="2xl" />
    </a>
    <a href="https://api.whatsapp.com/send?phone=56987216115&text=Hola+Yeferson%2C+quiero+contactarme+contigo+desde+tu+portafolio.
" target="_blank" rel="noopener noreferrer">
      <font-awesome-icon class="icons" icon="fa-brands fa-whatsapp" size="2xl" />
    </a>
    <a href="mailto:yefersonj.rr@gmail.com?Subject=Busco%20tu%20perfil%20desarrollador" target="_blank"
      rel="noopener noreferrer">
      <font-awesome-icon class="icons" icon="fa-solid fa-envelope" size="2xl" />
    </a>
  </div>
</template>

<script>
export default {
  name: 'IconSocialComponent'
}
</script>

<style scoped>
div {
  margin-top: 5rem;
  display: flex;
  justify-content: space-evenly;
}

a {
  color: inherit;
}
.icons:hover:hover {
  scale: 1.2;
  transition: 0.2s;
  color: rgb(226, 232, 240, 1);
  filter: drop-shadow(0 0 0.75rem rgb(226, 232, 240, 1));
}
</style>
  