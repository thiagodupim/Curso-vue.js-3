<template>
  <div>
    <theHeader>
      <template v-slot:title>
        Home
      </template>
      
      <template v-slot:description>
        <p>Dados</p>
      </template>

      Content do header - menu ... padrão
    </theHeader>
  </div>
</template>

<script>
  import TheHeader from './components/TheHeader.vue';

  export default {
    name: 'App', 
    components: { TheHeader },
    data() {
      return {

      }
    },
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
