<template>
  <div class="flex  justify-center bg-black min-h-screen font-alfa">
    <div class="flex flex-col ">
      <h1
        class="text-center  m-6 text-3xl px-20 py-4 rounded-2xl font-alfa font-normal text-rose-500 border-rose-500 border-2 hover:scale-105 duration-1000 hover:cursor-default ">
        My To-Do List</h1>
      <GerenciadorDeTasks @aoSalvarTarefa="salvarTarefa" />
      <div class="bg-white mt-10 pb-3 px-10 rounded-2xl">
        <h2 class="text-center text-2xl my-6 text-rose-500 rounded-2xl  py-2 bg-black">Your tasks</h2>
        <Tarefas v-for="(tarefa, indice ) in tarefas" :key="indice" :tarefa="tarefa" />
      </div>
    </div>
  </div>
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
  data() {
    return {
      tarefas: [] as ITarefa[]
    }
  },
  methods: {
    salvarTarefa(tarefa: ITarefa) {
      this.tarefas.push(tarefa)
      console.log(this.tarefas[0])
    }
  }
});
</script>

<style>

</style>
