<script setup>
import Counter from "./components/Counter.vue";
</script>

<template>
  <div class="app bg-slate-50">
    <header class="justify-start">
      <h1 class="text-4xl font-semibold text-center pt-5">Vue Playground</h1>
    </header>
    <div class="min-h-screen flex flex-col items-center justify-center">
      <Counter />
    </div>
  </div>
</template>
