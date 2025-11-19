<script setup>
import {ref, computed} from "vue"

const keyWord = ref("");
const items = ref(["apple", "banana", "grape", "orange"]);

const filterdList = computed(() => {
    return items.value.filter(item => item.toLowerCase().includes(keyWord.value.toLowerCase))
})
</script>


<template>

</template>