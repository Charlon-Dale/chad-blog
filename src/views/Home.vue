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
    console.log(this)

    const param = ref('hello')
    console.log(param, param.value)

    let name = 'mario'
    let age = 30

    const handleClick = () => {
      console.log(param, param.value)
      param.value.classList.add('test')
      param.value.textContent = 'hello, ninjas'
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
