<template>
    <div id="divPainel">
        <div id="painel">
            <input type="text" placeholder="Digite aqui.." v-model="tarefa"/>
        </div>
        <button @click="adcTarefa">Ok</button>
    </div>
  
</template>

<script>
export default {
name: 'TodoForm',
data: function() {
    return{
        tarefa: ''
    }
}, methods: {
        adcTarefa: function(){
            this.$emit('adctarefas', {
                tarefa: this.tarefa,
            })
            this.tarefa = '';
        }
    }

}
</script>

<style>
    #divPainel {
        width: 300px;
        height: 150px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        border: 0.50px solid rgb(6, 175, 197);
        box-shadow: 5px 10px 10px rgb(6, 175, 197);
        border-radius: 15px;
        margin-top: 50px;
        margin-left: 40%;
        
    }
    #painel {
        width: 60%;
        height: 28px;
        border-radius: 10px;
        background-color: #ffff;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #painel input {
      outline: none;  
      border: none;
    }
    #divPainel button {
        margin-top: 20px;
        cursor: pointer;
        width: 80px;
        border-radius: 5px;
        outline: none;  
    }
    #divPainel button:hover {
        transition: all 0.45s;
        color: white;
        width: 95%;
        background-color: rgb(6, 175, 197);
    }
</style>