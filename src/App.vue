<template>
  <div> 
    <Counter /> 
    <hr/>
    <Form /> 
    <hr/>
    <Body :text="text"/>
    <input type="text" v-model="text">
    <p>ccomputed</p>
    <BodyComputed :text="text"/>
    <hr/>
    <h1>watcher </h1>
    <watch />
    <hr>
    <div>
      <Lifecycle v-if="!show" />
      <button href="#" @click.prevent="destroy">destroy</button>
    </div>
    <br>
    <hr>
    <br>
    <MousePosition />
  </div>  
</template>
<script>
import { ref } from 'vue'
import Counter from './components/Counter.vue'
import Form from './components/Form.vue'
import Body from './components/Body.vue'
import BodyComputed from './components/BodyComputed.vue'
import Watch from './components/Watch.vue'
import Lifecycle from './components/Lifecycle.vue'
import MousePosition from './components/MousePosition.vue'

export default {
  components:{
    Counter,
    Form,
    Body,
    BodyComputed,
    Watch,
    Lifecycle,
    MousePosition
  },
  setup(){
    const text = ref('')
    const show = ref(true)
    function destroy(){
      show.value = !show.value
    }
    return {
      text,
      destroy
    }
  }
}
</script>