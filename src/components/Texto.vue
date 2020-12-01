<template>
  
  <span>
    Color: <input type="text" v-model="color">
  </span>

  <span>
    Fondo: <input type="text" v-model="bg">
  </span>

  <span>
    Size: <input type="text" v-model="size">
  </span>

  <hr>

  Texto: <input type="text" v-model="texto" :style="{'color': color, 'background-color': bg, 'font-size': size}">

  <p>
    Cantidad de palabras: {{cantidadPalabras}}
  </p>


  <table>
    <tr>
      <td>NRO PREG</td>
      <td>RESPUESTA</td>
    </tr>

    <tr>
      <td>1</td>
      <td>b</td>
    </tr>

    <tr>
      <td>2</td>
      <td>c</td>
    </tr>

    <tr>
      <td>3</td>
      <td>b</td>
    </tr>

    <tr>
      <td>4</td>
      <td>d</td>
    </tr>

    <tr>
      <td>5</td>
      <td>d</td>
    </tr>
  </table>

</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      color: '',
      bg: '',
      size: '',
      texto: ''
    }
  },
  computed:{

    cantidadPalabras(){
      let array = this.texto.split(" ")
      let contador = 0
      array.forEach(element => {
        if (element.trim() != "") contador ++
      });
      return contador
    }
    
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
