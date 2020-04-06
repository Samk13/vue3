<template>
  <div>
    <Counter />
    <Form />
    <Body :text="text"/>
    <input type="text" v-model="text">
    <p>ccomputed</p>
    <BodyComputed :text="text"/>
    <h1>watcher </h1>
    <watch />
  </div>  
</template>
<script>
import { ref } from 'vue'
import Counter from './components/Counter.vue'
import Form from './components/Form.vue'
import Body from './components/Body.vue'
import BodyComputed from './components/BodyComputed.vue'
import Watch from './components/Watch.vue'

export default {
  components:{
    Counter,
    Form,
    Body,
    BodyComputed,
    Watch
  },
  setup(){
    const text = ref('')

    return {
      text,
    }
  }
}
</script>