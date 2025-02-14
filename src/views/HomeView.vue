<script setup>
import {useCounterStore} from '@/stores/counter';
import Counter from "@/components/Counter.vue";

const storeCounter = useCounterStore();
</script>

<template>
  <div class="home">
    <Counter/>
    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
    <hr>
    <div>
      The counter is: {{ storeCounter.oddOrEven }}
    </div>
    <hr>
    <h3>Edit Counter:</h3>
    <input v-model="storeCounter.count" type="number"/>
  </div>
</template>

<style>
.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
