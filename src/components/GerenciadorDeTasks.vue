<template>
    <section class="section-gerenciamento">   
        <input 
            type="text" 
            placeholder="enter your task here" 
            @input="escrevendo"
            v-model="descricao"
        />
        <button 
            :disabled="!inputTask" 
            v-bind:class="{'ativado': ativando}"
            @click="adicionarTasks">
            Add
        </button>
    </section> 
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import ITarefa from './interfaces/ITarefa';

export default defineComponent({
    name: 'GerenciadorDeTasks',
    data (){
        return{
            inputTask: false,
            ativando: false,
            descricao: '',
            tarefas: [] as ITarefa[]
        

        }
    },
    methods:{
        escrevendo () {
            this.inputTask = true
            this.ativando = true
        },
        adicionarTasks (){
            console.log(this.descricao)
            this.descricao = ''
        }
    },
})
</script>

<style scoped>
.section-gerenciamento{
    display: flex;
    justify-content: center;
}
input{
    padding: 10px 20px;
    width: 300px;
    border-radius: 10px;
    font-size: 20px;
    background-color: white;
    color: black;
    border: 4px solid black;
}
button{
    border-radius: 20px;
    cursor: pointer;
    font-size: 15px;
    font-style: italic;
    background-color: white;
    color: black;
    font-weight: bold;
    transition: .5s;
    border: 4px solid black;
}
.ativado:hover{
    background-color: black;
    color: white;
    border-color: white;
    scale: 1.02;
    opacity: 1;
} 
button:disabled{
    opacity:.5 ;
}
</style>