<script setup>
import {ref} from "vue"

const inputRef = ref()

const click = () => {
    inputRef.value.focus();
}

alert(inputRef.value);

</script>

<template>
      <div>
    <input
      type="text"
      ref="inputRef"
      v-model="inputValue"
    />

    <button @click="handleClick">버튼</button>
  </div>


</template>