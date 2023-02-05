<template>
    <div class="mt-5     flex justify-between" v-bind:class="{ 'hide': invisivel }">
        <div class="flex">
            <div class="w-6 mr-2 border-2 border-black hover:cursor-pointer" 
                @click="deixarMarcado"
           ><img src="../assets/verificar.png" alt="Concluído" v-bind:class="{ 'hide': !concluido }"></div>
            <p class="text-1xl "  v-bind:class="{ 'line-through': concluido}">
                - {{ tarefa.descricao }}
            
            </p>
        </div>
        <button @click="deixarinvisivel"><img src="../assets/lixo.png" alt="remover" class="w-5"></button>
    </div>

</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import ITarefa from './interfaces/ITarefa';

export default defineComponent({
    name: 'Tarefas-Descricoes',
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            required: true
        }
    },
    methods: {
        deixarinvisivel() {
            this.invisivel = true
        },
        deixarMarcado(){
            if(this.concluido === true){
                this.concluido = false
            }
            else if(this.concluido === false){
                this.concluido = true
            }
        }
    },
    data() {
        return {
            invisivel: false,
            concluido: false
        }
    }
})
</script>

<style scoped>
.hide {
    display: none;
}
</style>