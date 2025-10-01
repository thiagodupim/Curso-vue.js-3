<template>
  <div>
    <input v-model="name" type="text"> <br>
    {{ name }}

    <br><br><br>

    <input v-model="user.first_name" type="text"> <br>
    <input v-model="user.last_name" type="text"> <br>
    {{ user.first_name }} {{ user.last_name }}

    <br><br><br>

    <select v-model="pageCount">
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="15">15</option>
    </select> <br>
    {{ pageCount }}
  </div>
</template>

<script>
export default {
  name: 'App', 
  data() {
    return {
      name: '',
      pageCount: 5,
      user: {
        first_name: '',
        last_name: '',
      }
    }
  },

  watch: {
    name(value) {
      if (value.length >= 3) {
        this.saveUserName();
      }
    },
    pageCount() {
      this.changePage();
    },
    user: {
      handler() { // Handler significa que quando o objeto alterar é para executa-lo
        console.log('User alterado');
      },
      deep: true // Quando qualquer coisa dentro do o objeto se alterar dispare o código acima, então para observar o objeto profundamente precisamos transformar em deep
    },
  },

  computed: {
    
  },

  methods: {
    saveUserName() {
      console.log('Ajax');
      console.log(this.name);
    },
    changePage() {
      console.log('Ajax changePage')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
