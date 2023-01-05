<template>
  <Cabecalho/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Cabecalho from './components/Cabecalho.vue';

export default defineComponent({
  name: 'App',
  components: {
    Cabecalho
  }
});
</script>

<style>
@import url(./assets/css/reset.css);
@import url('https://fonts.googleapis.com/css2?family=Kaushan+Script&display=swap');
#app{
  font-family: 'Kaushan Script', cursive;
  width: 100%;
  height: 100vh;
  background: linear-gradient(90deg, #00C9FF 0%, #92FE9D 100%); 
}
</style>
