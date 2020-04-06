<template>
<div>
    <p>counter</p>
    <a href="#" @click.prevent="increment">Increment</a> {{ number }}
</div>
</template>
<script>
import { ref } from 'vue'
export default {
    setup(){
        const number = ref(0)
        function increment(){
            number.value ++
        }
     return{
         number,
         increment
     }
    }
}
</script>

<style>

</style>