<script setup>
import ConditionalRendering from "./components/ConditionalRendering.vue";
import Counter from "./components/Counter.vue";
import Iteration from "./components/Iteration.vue";
</script>

<template>
  <div class="app bg-slate-50">
    <header class="bg-slate-900">
      <h1 class="text-4xl font-semibold text-center text-slate-50 py-5">
        Vue Playground
      </h1>
    </header>
    <div class="min-h-screen flex flex-col items-center justify-center">
      <Counter />
    </div>
    <div
      class="min-h-screen bg-slate-700 text-gray-100 flex flex-col items-center justify-center"
    >
      <ConditionalRendering />
    </div>
    <div
      class="min-h-screen bg-green-100 text-gray-100 flex flex-col items-center justify-center"
    >
      <Iteration />
    </div>
  </div>
</template>
