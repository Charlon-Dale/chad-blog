<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  setup() {
    console.log('setup')

    let name = 'mario'
    let age = 30

    return { name: name, age: age }

  }
}
</script>
