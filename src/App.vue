<template>
  <div>
    
    <h2>Parent Component</h2>
    <!-- <button @click="sendMessage">Child ko message bhejo</button> -->
    <p>Child Message Recevied: {{ parentMessage }}</p>

    <child message = 'hello from parent' @childEvent="updateMessage" />

    
    
  </div>
</template> 

<script setup>
import child from './child.vue';
import { ref } from 'vue';


const props = defineProps(['Parent'])


const parentMessage = ref('');

const updateMessage = (message) => {
  parentMessage.value = message;
};
</script>


