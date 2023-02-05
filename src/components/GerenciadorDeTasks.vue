<template>
    <section class="section-gerenciamento">   
        <input class="border-rose-500 border-2 mt-10 px-10 py-2 rounded-2xl text-rose-500 "
            type="text" 
            placeholder="Enter your task here" 
            @input="escrevendo"
            v-model="descricao"
            @keydown.enter="adicionarTasks"
        />
        <button 
            :disabled="!inputTask" 
            v-bind:class="{'ativado': estilo}"
            @click="adicionarTasks"
            >
            
            Add
        </button>
    </section> 
</template>

<script lang="ts">
import { defineComponent } from 'vue';



export default defineComponent({
    name: 'GerenciadorDeTasks',
    data (){
        return{
            inputTask: false,
            estilo: false,
            descricao: '',
            }  
        },
    methods:{
        escrevendo () {
            this.inputTask = true
            this.estilo = true

        },
        adicionarTasks (){
            this.inputTask = false
            this.estilo = false
            this.$emit('aoSalvarTarefa', { descricao: this.descricao })
            this.descricao = ''
        }
    },
    emits:['aoSalvarTarefa']

})
</script>

<style scoped>

</style>