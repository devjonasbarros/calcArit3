<template>

<h1>CALCULADORA EBAC !</h1> <br> <br>
    <input v-model="a" placeholder="Number 1"/> <br> <br>
    <input v-model="b" placeholder="Number 2"/> <br> <br>

    <div>
    <select v-model="selectedValue">
      <option disabled value="">Selecione aritmetica</option>
      <option>Adicao</option>
      <option>Subtracao</option>
      <option>Multiplicacao</option>
      <option>Divisao</option>
    </select>
  
  </div>


    <br>
    <br>
    <br>
    <hr>


  <p class="resul">Resultado: {{ multi() }}</p>
  

  <p>Primeiro Valor digitado foi: {{ a }}</p>
  <p>Segundo Valor informado foi: {{ b }}</p>
  <p>A operação selecionada foi: {{ selectedValue }}</p>
  
</template>

<script>
export default {
  data(){
    return{
      a: '',
      b: '',
      selectedValue: ''
    }
  },
  methods:{
  
    somar(){
      return this.a + this.b;

    }, 
    multi(){
      return this.a * this.b;
    },
    divis(){
      return this.a / this.b;
    },

    sub(){
      return this.a - this.b
    }
    
  }
}

</script>

<style>

input{
  width: 220px;
  height: 30px;
}

select{
  width: 220px;
  height: 30px;
}

a{
  color: red;
  font-size: 22px;
  font-family: Arial, Helvetica, sans-serif;
}

.resul{
  background-color: rgb(204, 204, 35);
  color: black;
  font-size: 22px;
  font-family: Arial, Helvetica, sans-serif;
  height: 50px;
  width: 380px;
  padding:  10px;
}



</style>