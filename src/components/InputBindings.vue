<script setup>
import { reactive, ref } from "vue";

const message = ref("");
const formData = reactive({
  username: "",
  email: "",
  password: "",
});
</script>

<template>
  <div class="text-slate-900 space-y-5">
    <div class="bg-green-300 p-4 rounded-md shadow-md shadow-black/5">
      <p>Message is: {{ message }}</p>
      <input
        class="p-2 border w-full rounded-md mt-3"
        v-model="message"
        type="text"
        placeholder="type a message"
      />
    </div>

    <div class="bg-green-300 p-4 rounded-md shadow-md shadow-black/5">
      <form @submit.prevent="">
        <input
          class="p-2 border w-full rounded-md mt-3"
          type="text"
          placeholder="enter your name"
          v-model="formData.username"
        />
        <input
          type="email"
          class="p-2 border w-full rounded-md mt-3"
          placeholder="enter your email"
          v-model="formData.email"
        />
        <input
          type="password"
          class="p-2 border w-full rounded-md mt-3"
          placeholder="enter password"
          v-model="formData.password"
        />
        <button
          type="submit"
          class="mt-3 px-4 py-2 bg-green-50 rounded-md font-medium"
        >
          Submit
        </button>
      </form>

      <div class="mt-5">
        <p class="font-semibold text-lg">Username: {{ formData.username }}</p>
        <p class="font-semibold text-lg">Email: {{ formData.email }}</p>
        <p class="font-semibold text-lg">Password: {{ formData.password }}</p>
      </div>
    </div>
  </div>
</template>
