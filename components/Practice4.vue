<script setup>
import {reactive , computed} from "vue"


const cart = reactive({
  item1: {
    price: 10000,
    count: 2
  },
  item2: {
    price: 3000,
    count: 2
  }
});

const totalPrice = computed(() => {
    return cart.item1.price * cart.item1.count + cart.item2.price * cart.item2.count
    
})

</script>

<template>
    <h1>item1: {{ cart.item1.price }}원 {{ cart.item1.count }}개</h1>
    <h1>item2: {{ cart.item2.price }}원 {{ cart.item2.count }}개</h1>

    <h2>합계 : {{ totalPrice }}</h2>


</template>