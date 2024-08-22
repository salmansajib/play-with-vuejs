<script setup>
import { ref } from "vue";

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
</script>

<template>
  <div class="container mx-auto flex flex-col items-center justify-center pt-3">
    <h1 class="text-5xl font-medium text-center mt-5">Counter App</h1>
    <p class="text-3xl py-5">
      Count is :
      <span
        :class="{ 'text-blue-500': count > 0, 'text-red-500': count < 0 }"
        >{{ count }}</span
      >
    </p>
    <div class="flex items-center gap-2 pt-3">
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
