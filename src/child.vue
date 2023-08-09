<template>
    <div class="child">
      <h3>Child Component</h3>
      <button @click="sendMessage">Parent ko message bhejo</button>
      <p>Parent Message : {{ message }}</p>
    </div>
  
  </template>
  
<script setup>


const props = defineProps(['message'])
let nm = (props.message.toUpperCase())


const emits = defineEmits(['childEvent']);

const sendMessage = () => {
  console.log('child')
  emits('childEvent', nm);
};
</script>


