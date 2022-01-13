<template>
  <button @click="clickHandler">Button 1</button>
</template>

<script>
export default {
name: "MyButton",
emits: {
    'custom-event-1':null, 
    'custom-event-2' (payload) {
        return !!(payload.name && payload.role)
    }
},
    methods: {
        clickHandler(){
            this.$emit('custom-event-1', 'data1');
            this.$emit('custom-event-2', {
                name: 'Vasya',
                role: "Admin"
            });
        }
    },
}
</script>

<style>

</style>