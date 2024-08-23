<script setup>
import { ref } from "vue";

const toggleValue = ref(true);
</script>

<template>
  <div>
    <h1 class="pb-5 text-2xl font-semibold">
      Vue is <span v-if="toggleValue">Awesome</span> <span v-else>Meh</span>!
    </h1>
    <button
      @click="toggleValue = !toggleValue"
      class="border border-gray-100 rounded-md px-4 py-2"
    >
      Toggle
    </button>
  </div>
</template>
