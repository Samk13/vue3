<template>
    <div>
        <p>{{ apperCase }}</p>
    </div>
</template>
<script>
import { computed } from 'vue'

export default {
    props:{
        text:{
            required: true,
            type: String,
        },
    },
setup(props){
    const apperCase = computed(() => props.text.toUpperCase())

    return {
        apperCase
    }
}
 }
</script>