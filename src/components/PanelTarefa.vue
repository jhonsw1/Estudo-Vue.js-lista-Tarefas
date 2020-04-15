<template>
   <div id="panelTarefa">
       <div id="tarefas" v-for="(adcTarefa, index) in arreyTarefas" :key="index">
            <span>{{adcTarefa}}</span>
       </div>

   </div>
</template>

<script>
export default {
name: "PanelTarefa",
props: ['arreyTarefas']
}
</script>

<style>
    #panelTarefa {
        width: 600px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        min-height: 200px;
        margin-top: 200px;
        margin-left: 32%;
        border-radius: 10px;
        border: 0.50px solid rgb(6, 175, 197);
        box-shadow: 5px 10px 10px rgb(6, 175, 197);
    }
    #tarefas {
        background-color: #fff;
        color: black;
        width: 30%;
        margin-top: 30px;
        margin-left: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 5px;
        cursor: pointer;
        
    }
    #tarefas:hover {
        transition: all 1.70s;
        background-color: black;
        color: #fff;
        border: 1px solid #fff;
    }
</style>