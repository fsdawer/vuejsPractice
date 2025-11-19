<script setup>
   import {computed, reactive, ref} from 'vue';

   const refCount = ref(0);  // ref 값 설정법 
   const reactiveCount = reactive({count : 0});   // reative 값 설정법 

   
   // ref() 데이터를 활용시 value 속성 사용
   const refDoubleCount = computed({
  get() {
    return refCount.value * 2;
  },
  set(newValue) {
    refCount.value = newValue;
  },
});

  // reactive() 데이터는 .value 속성 필요 없음
const reactiveDoubleCount = computed({
  get() {
    return reactiveCount.count * 2;
  },
  set(newValue) {
    reactiveCount.count = newValue;
  },
});


setTimeout(() => {
  refCount.value = 10;
  reactiveCount.count = 20;
}, 1000);
console.log(refDoubleCount.value);
console.log(reactiveDoubleCount.value);

</script>

<template>
    <h1>{{ refDoubleCount }}</h1>
    <h1>{{ reactiveDoubleCount }}</h1>
</template>