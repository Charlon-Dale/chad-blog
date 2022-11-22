<template>
  <div class="home">
    home
    <p ref="param">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Home',
  setup() {
    //const p = ref(null)
    
    const name = ref('mario')
    const age = ref(30)

    const handleClick = () => {
      name = 'luigi'
    }

    return { name, age, handleClick, param }
  },
  data() {
    return {
      age: 40
    }
  }
}
</script>
