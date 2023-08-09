<template>
    <div class="child">
      <h3>Child Component</h3>
      <button @click="sendMessage">Parent ko message bhejo</button>
      <p>Parent Message : {{ message }}</p>
    </div>
  
  </template>
  
<script setup>



const props = defineProps(['message'])
console.log(props.message)
const emits = defineEmits(['childEvent']);

const sendMessage = () => {
  let nm = (props.message.toUpperCase())
  console.log(nm)
  emits('childEvent', nm);
};
</script>


