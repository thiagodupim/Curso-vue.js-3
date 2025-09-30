<template>
  <div>
    <h1 :class="{ 'title': true, 'title-home': isHome }">
      Curso VueJS 3
    </h1>

    <p :class="pClass">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quaerat provident reprehenderit distinctio! Consequuntur, error harum, asperiores eaque perspiciatis unde illum corrupti assumenda, sapiente deserunt atque. Illo aut iusto neque dolore.
    </p>

    <p :style="styleClass">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem cum exercitationem fuga aperiam alias dolores tenetur quasi voluptatem voluptatibus porro ipsam optio incidunt cupiditate facere, illo esse, ipsum fugit sunt.
    </p>

    <div 
      v-for="(obj, index) in todos" 
      :key="obj.id" 
      class="todos-item"
      >
      <img 
        v-if="obj.imgSrc" 
        :src="obj.imgSrc"
      >
      {{ index }} - {{ obj.title }}
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheHeader from './components/TheHeader';

export default {
  name: 'App', 
  data() {
    return {
      isHome: true,
      classVar: 'title',
      styleClass: { color: 'aqua', backgroundColor: 'black', 'font-size': '20px' }, // Conseguimos fazer das duas formas
      pClass: ['text', 'text-home'],
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc": 'https://placehold.co/150'
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc": 'https://placehold.co/150'
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
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
