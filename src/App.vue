<template>
  <div id="app">
    <TodoForm @adctarefas="adcTarefa($event)"/>
    <panel-tarefa :arreyTarefas="Tarefas"/>
  </div>
</template>

<script>
import TodoForm from './components/TodoForm.vue';
import PanelTarefa from './components/PanelTarefa.vue';
export default {
  name: 'App',
  components: {
  TodoForm,
  PanelTarefa
  }, data: function(){
    return {
      Tarefas: []
  }
  }, methods: {
     
    adcTarefa: function(event) {
      this.Tarefas.push(event.tarefa) 
    }
  }
}
</script>

<style>

</style>
