<template>
 <header class="bg-blue-500">
    <h1>My To-Do List</h1>
    <GerenciadorDeTasks @aoSalvarTarefa="salvarTarefa"/>
    <Tarefas v-for="(tarefa, indice ) in tarefas" :key="indice" :tarefa="tarefa" />
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import GerenciadorDeTasks from './components/GerenciadorDeTasks.vue';
import Tarefas from './components/Tarefas.vue';
import ITarefa from './components/interfaces/ITarefa';

export default defineComponent({
  name: 'App',
  components: {
    GerenciadorDeTasks,
    Tarefas
  },
  data(){
    return{
      tarefas: [] as ITarefa[]
    }
  },
  methods:{
    salvarTarefa (tarefa: ITarefa){
      this.tarefas.push(tarefa)
      console.log(this.tarefas[0])
    }
  }
});
</script>

<style>

</style>
