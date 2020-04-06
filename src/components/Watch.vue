<template>
  <p>{{ number }}</p> 
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const number = ref(0)
    setInterval(() => { number.value += 1},500)
    return {
      number,
    }
  }
}
</script>

<style>

</style>