<script setup>
import { ref } from "vue";

const toggleValue = ref(true);
</script>

<template>
  <div class="w-[300px]">
    <h1 class="pb-5 text-2xl font-semibold max-w-max">
      Vue is
      <span class="text-blue-500" v-if="toggleValue">Awesome!</span>
      <span class="text-red-500" v-else>Meh!</span>
    </h1>
    <button
      @click="toggleValue = !toggleValue"
      class="bg-gray-100 text-slate-900 font-semibold rounded-md px-4 py-2"
    >
      Toggle
    </button>
  </div>
</template>
