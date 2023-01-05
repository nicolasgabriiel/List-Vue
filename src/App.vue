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
</style>
