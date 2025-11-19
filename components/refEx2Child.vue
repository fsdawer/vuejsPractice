<script setup>
import { computed, ref } from 'vue';

const number = ref(5);
const doubleNumber = computed(()=> number.value * 10);

defineExpose( // defineExpose 지정한 값만 부모컴포넌트에서 접근 가능 
    {
        number, 
        doubleNumber,
    }
);
</script>


<template>
    <h1>{{ number }}</h1>
    <h1>{{ doubleNumber }}</h1>
</template>
