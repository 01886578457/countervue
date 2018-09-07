<template>
 <button @click="handleClick"><slot></slot></button>
</template>

<script>
export default {
    name: "CounterButton",
    methods:{
        handleClick(){
            this.$emit('clicked')
        }
    }
}

</script>
