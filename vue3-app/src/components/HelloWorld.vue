<template>
  <!-- <div class="hello">
    <teleport to=".my-div">
      <p>From Teleport</p>
    </teleport>
  </div>
  <button @click="toggleModal">Show/hide</button>
  <teleport to="#modal">
    <my-modal v-if="showModal">
      <p>From Modal</p>
      <button @click="toggleModal">Close</button>
    </my-modal>
  </teleport>
  <br/>
  {{ user }}
  <login-form v-model:username="user.name" v-model:password="user.password"/> -->
  <br/>
  <button @click="someMethod">{{ count }}</button>
  <!-- <button @click="addLink">Add Link</button>
  <button @click="removeLink">Remove Link</button>
  <my-button @custom-event-1="firstEvent" @custom-event-2="secondEvent" /> -->
</template>

<script setup>
// import MyButton from "./MyButton.vue";
// import MyModal from "./MyModal.vue";
// import LoginForm from "./LoginForm.vue";
import { nextTick, onMounted, ref } from 'vue'
const count = ref(0)
console.log(count.value)
console.log(count)
onMounted(async()=>{
 await nextTick(()=>{})
})

const someMethod= ()=>{
  count.value++
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
