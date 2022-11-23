<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <p> search term - {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">{{ name }}</div>
    <button @click="handleClick">Stop watching</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Home',
  setup() {
    const posts = ref([
      { title: 'Welcome to the blog', body: 'Lorem ipsum', id: 1 },
      { title: 'top 5 CSS tips', body: 'lorem ipsum', id: 2 },
    ])
    
    return { posts }
  }
}
</script>
