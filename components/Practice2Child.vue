<script setup>
import {defineProps, defineEmits} from "vue"

// 부모에게 받은 데이터
const props = defineProps({
    name: String
})

// 부모에게 다시 이벤트 보낼 준비
const emit = defineEmits(['greet'])

// 자식 내부에서 부모 이벤트 호출
const sendGreeting = () => {
    emit('greet', `Hello, ${props.name}!`);
}
</script>


<template>
   <div>
    <button @click="sendGreeting">Send Greeting</button>
  </div>
</template>