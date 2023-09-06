<template>
  <div id="app">
    <HelloWorld/>
    <div class="cursor" :style="{ top: cursorY + 'px', left: cursorX + 'px' }"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      cursorX: 0,
      cursorY: 0,
    }
  },
  components: {
    HelloWorld
  },
  methods: {
    trackCursor(event) {
      this.cursorX = event.clientX;
      this.cursorY = event.clientY ;
    },
  },
  created() {
    window.addEventListener("mousemove", this.trackCursor);
  },
  destroyed() {
    window.removeEventListener("mousemove", this.trackCursor);
  }
}
</script>

<style>
body, html {
  margin: 0;
  padding: 0;
  height: 200vh; 
  scroll-behavior: smooth;
}
*, *:before, *:after {
  box-sizing: inherit;
}

 button{
  margin: 20px;
  background: transparent;
  color: rgb(226, 232, 240, 1);
  border:none;
  cursor: pointer
  
}

html{
    background: linear-gradient(-90deg ,rgb(10, 29, 67), rgb(15, 31, 54), rgb(6, 29, 81));
    background-size: 400% 400%;
    animation: gradient 12s ease infinite;
    height: 200vh;
}

@keyframes gradient {
    0% {
        background-position: 0% 50%;
    }
 
    50% {
        background-position: 100% 50%;
    }
 
    100% {
        background-position: 0% 50%;
    }
}
@media (min-width: 1024px ){ 
    .cursor {
  position:fixed;
  width: 100px;
  height: 100px;
  filter: blur(5rem);
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  pointer-events: none;
 
}
}

#app {
  color: rgb(148, 163, 184, 1);
}
</style>
