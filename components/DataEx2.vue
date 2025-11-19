<script setup>
    import {ref} from 'vue';

    const arr1 = ref([10]);  // 배열로 반응형 데이터 생성
    const arr2 = ref([10]);

    setTimeout(
        () => {arr1.value = [10,20];
        },1000
    );

    setTimeout(
        () => {arr2.value.push(20)}, 1000
    );   // 배열 요소 변경 (추가)

</script>


<template>
<h1>count : {{ arr1 }}</h1>
<h1>state : {{ arr2 }}</h1>

</template>