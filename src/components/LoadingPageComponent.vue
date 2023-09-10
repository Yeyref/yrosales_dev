<template>
    <div class="loading-overlay" :class="{ 'loading-overlay2': loaded }" id="loader">
        <div class="lds-ripple">
            <div></div>
            <div></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LoadingPageComponent',
    data: function(){
        return {
            loaded: false,
        }
    },
    mounted() {   
      setTimeout(() => {
        this.loaded = true;
      }, 1000);
  },
}
</script>

<style scoped>

.loading-overlay{
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(-90deg ,rgb(6, 17, 38), rgb(15, 31, 54), rgb(3, 16, 45));
  background-size: 400% 400%;
  z-index: 1000;
  clip-path: circle(141.2% at 100% 0);
  transition: clip-path 0.8s ease-in-out;
  overflow: hidden;
}

.loading-overlay2{
    clip-path: circle(0 at -90% -100%);
}

.lds-ripple {
  display: inline-block;
  position: relative;
  width: 72px;
  height: 72px;
}

.lds-ripple div {
  position: absolute;
  border: 4px solid #fff;
  opacity: 1;
  border-radius: 50%;
  animation: lds-ripple 1s cubic-bezier(0, 0.2, 0.8, 1) infinite;
}

.lds-ripple div:nth-child(2) {
  animation-delay: -0.5s;
}

@keyframes lds-ripple {
  0% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 0;
  }
  4.9% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 0;
  }
  5% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 1;
  }
  100% {
    top: 0px;
    left: 0px;
    width: 72px;
    height: 72px;
    opacity: 0;
  }
}
</style>