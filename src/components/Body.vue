<template>
    <div>
        <p>{{ text }}</p>
    </div>
</template>

<script>
export default {
    props:{
        text:{
            required: true,
            type: String,
        }
    },
    setup(props){
        console.log(props.text);
     }
    }
</script>