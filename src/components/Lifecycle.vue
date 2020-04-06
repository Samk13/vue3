<template>
    <div>
        <h1>Life cycle</h1>
    </div>
</template>

<script>
import { onMounted, onUnmounted } from 'vue'
export default {
    setup(){
       onMounted(() => {
            console.log(`Component is now mounted `);
        })
       onUnmounted(() => {
            console.log(`Component is Unmounted `);
        })
        }
    }
</script>