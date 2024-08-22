<script setup>
import { computed, ref } from "vue";

const count = ref(0);

const increment = () => {
  count.value++;
};
const decrement = () => {
  count.value--;
};
const reset = () => {
  count.value = 0;
};
const doubleCount = computed(() => {
  return count.value * 2;
});
const tripleCount = computed(() => {
  return count.value * 3;
});
</script>

<template>
  <div class="container mx-auto flex flex-col items-center justify-center pt-3">
    <h1 class="text-5xl font-medium text-center mt-5">Counter App</h1>
    <p class="text-3xl pt-10 font-semibold">
      Count is :
      <span :class="count >= 0 ? 'text-blue-500' : 'text-red-500'">{{
        count
      }}</span>
    </p>
    <p class="text-3xl pt-5 font-semibold">Double Count : {{ doubleCount }}</p>
    <p class="text-3xl pt-5 font-semibold">Triple Count : {{ tripleCount }}</p>
    <div class="flex items-center gap-2 pt-5">
      <button
        @click="increment"
        class="bg-green-700 text-slate-50 px-4 py-2 rounded-md"
      >
        Increment
      </button>
      <button
        @click="reset"
        class="bg-red-700 text-slate-50 px-4 py-2 rounded-md"
      >
        Reset
      </button>
      <button
        @click="decrement"
        class="bg-blue-700 text-slate-50 px-4 py-2 rounded-md"
      >
        Decrement
      </button>
    </div>
  </div>
</template>
