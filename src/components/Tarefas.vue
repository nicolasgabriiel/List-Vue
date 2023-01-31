<template>
    <div>{{tarefa.descricao}}</div>
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
    }
})
</script>
