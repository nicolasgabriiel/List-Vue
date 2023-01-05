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

</style>
