<template>
  <div class="home">
Home
<p ref="p">My name is {{ name }} and my age is {{ age }}</p>
<button @click="handleClick">Click me</button>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  name: 'Home',
  setup() {
    // const p = ref(null)


    const name = ref('mario')
    const age = ref(18)

    const handleClick = () => {
      name.value = 'luigi'
      age.value = 20
    }

    return { name, age, handleClick }
  }
}
</script>
