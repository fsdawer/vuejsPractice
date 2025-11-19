<script setup>
import {ref, computed} from "vue"

const searchText = ref("");

// 삼항연산자 사용해서 참이면 10자초과 문구
const warningMessage = computed(() => {
    if(searchText.value.length > 10) {
        return "10자 초과했습니다"
    }
    return "";
});

</script>


<template>
    <!-- v-model = 양방향 바인딩 -->
    <div>
        <input type="text" v-model="searchText"></input>
    </div>


</template>