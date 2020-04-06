<template>
    <div>
        <h1>mouse data</h1>
        <h2>x = {{ x }}</h2>
        <h2>y = {{ y }}</h2>
    </div>
</template>
<script>
import { useMousePosition } from '../Tools/mouse.js'
export default {
    setup(){
        const {x,y} = useMousePosition()
        
        return{
            x,
            y
        }
    }
}
</script>

<style>

</style>