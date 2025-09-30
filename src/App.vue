<template>
  <div>
    <div>
      One-way data binding <br>
      Two-way data binding <br>
      v-model -> formulários
    </div>

    <br> <br>

    <input v-model="name" type="text">
    
    <br>

    {{ name }}

    <br> <br>

    <div>
      <label>Sports</label> <br>
      <select v-model="sports">
        <option value="">Escolha</option>
        <option value="futebol">Futebol</option>
        <option value="skate">Skate</option>
        <option value="tenis">Tenis</option>
      </select> <br>
      {{ sports }}
    </div>

    <br> <br>

    <div>
      <label>Newsletter</label> <br>
      <input v-model="newsletter" type="radio" value="Sim"> Sim
      <input v-model="newsletter" type="radio" value="Não"> Não <br>
      {{ newsletter }}
    </div>

    <br> <br>

    <div>
      <label>Contrato</label> <br>
      <input v-model="contract" type="checkbox"> Aceita nossos termos... <br>
      {{ contract }}
    </div>

    <br> <br>

    <div>
      <label>Cores que você mais gosta</label> <br>
      <input v-model="colors" type="checkbox" value="Azul"> Azul <br>
      <input v-model="colors" type="checkbox" value="Amarelo"> Amarelo <br>
    </div>
    {{ colors }}
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheHeader from './components/TheHeader';

export default {
  name: 'App', 
  data() {
    return {
      name: 'Thiago Dupim',
      sports: 'futebol',
      newsletter: 'Não',
      contract: false,
      colors: []
    }
  }
}
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}

.title-home {
  font-size: 40px;
  color: green;
}

.text {
  color: yellow;
}

.text-home {
  color: #42b983;
}

.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
