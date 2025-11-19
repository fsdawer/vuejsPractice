<script setup>
import {ref, computed, watch} from "vue"

const count = ref(0);

// computed = 값을 계산하는 용도
// 값을 변경하는(action)” 용도로 쓰면 안 됨.
const doubledCount = computed(()=> count.value * 2);

// 그래서 increment는 함수로 만들어서 사용
const increment = () => {
    count.value++;
};

watch(count, (newVal, oldVal) => {
  console.log(`Count changed from ${oldVal} to ${newVal}`);
});

</script>


<template>
    <div>
        <p>Count: {{ count }}</p>
        <p>Doubled Count: {{ doubledCount }}</p>
        <button @click="increment">increment</button>
    </div>

</template>