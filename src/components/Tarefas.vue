<template>
    <div v-bind:class="{'hide': invisivel}">
        <div>{{tarefa.descricao}}</div>
        <button @click="deixarinvisivel">remove</button>
    </div>
    
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import ITarefa from './interfaces/ITarefa';

export default defineComponent({
    name:'Tarefas-Descricoes',
    props:{
        tarefa:{
            type: Object as PropType<ITarefa>,
            required: true
        }
    },
    methods:{
        deixarinvisivel(){
            this.invisivel = true
        }
    },
    data(){
        return{
            invisivel: false
        }
    }
})
</script>

<style scoped>
.hide{
    display: none;
}
</style>