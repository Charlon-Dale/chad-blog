<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <p> search term - {{ search }}</p>
    <div v-for="name in names" :key="name">{{ name }}</div>
  </div>
</template>

<script>
import { ref, computed } from 'vue'

export default {
  name: 'Home',
  setup() {
    const search = ref('')
    const names = ref(['mario', 'yoshi', 'luigi', 'toad', 'bowser', 'koopa', 'peach'])

    return { names, search }
  }
}
</script>
