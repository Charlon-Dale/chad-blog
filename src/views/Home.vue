<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Home',
  setup() {
    console.log(this)

    const param = ref(null)

    let name = 'mario'
    let age = 30

    const handleClick = () => {
      console.log('You clicked me')
    }

    return { name, age, handleClick, p }
  },
  data() {
    return {
      age: 40
    }
  }
}
</script>
