<script setup>
import {ref} from 'vue';
const inputRef = ref(null);

setTimeout(  // 1초뒤에 콜백함수를 실행
    () => {
        console.log(inputRef.value) // h1 태그에 해당하는 돔객체
        console.log(inputRef.value.innerText)  // 돔 객체의 속성, 메소드 모두 사용
    }, 1000
);

</script>


<template>
    <h1 ref="inputRef">hello, ref!</h1>
</template>
