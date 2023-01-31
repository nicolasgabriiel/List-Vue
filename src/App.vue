<template>
 <header>
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
@import url(./assets/css/reset.css);
@import url('https://fonts.googleapis.com/css2?family=Kaushan+Script&display=swap');
#app{
  font-family: 'Kaushan Script', cursive;
  width: 100%;
  height: 100vh;
  background: linear-gradient(90deg, #00C9FF 0%, #92FE9D 100%); 
}
h1{
  text-align: center;
  padding: 50px 0 ;
  font-size: 50px;
}
</style>
