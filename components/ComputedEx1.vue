<script setup>
   import {computed, reactive, ref} from 'vue';

   const refCount = ref(0);  // ref 값 설정법 
   const reactiveCount = reactive({count : 0});   // reative 값 설정법 

   const refDoubleCount = computed(() => refCount.value * 2) // ref() 데이터를 활용시 .value 속성 활용
   const reactiveDoubleCount = computed(() => reactive * 2)  // reactive() 데이터는 .value 속성 필요 없음

   console.log(refDoubleCount.value);
   console.log(reactiveDoubleCount.value);    // computed로 계산된 값을 출력할때는 value 사용
</script>

<template>
    <h1>{{ refDoubleCount }}</h1>
    <h1>{{ reactiveDoubleCount }}</h1>
</template>