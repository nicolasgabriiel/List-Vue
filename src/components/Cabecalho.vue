<template>
  <header>
    <h1>My To-Do List</h1>
    <GerenciadorDeTasks/>
  </header>
</template>

<script lang="ts">

import { defineComponent } from 'vue';
import GerenciadorDeTasks from './GerenciadorDeTasks.vue';

export default defineComponent({
  name: 'cabecalho-principal',
  components: {
    GerenciadorDeTasks
  }
 
});
</script>

<style scoped>
h1{
  text-align: center;
  padding: 50px 0 ;
  font-size: 50px;
}
</style>
