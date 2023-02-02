<template>
    <section class="section-gerenciamento">   
        <input 
            type="text" 
            placeholder="enter your task here" 
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