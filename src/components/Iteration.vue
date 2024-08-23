<script setup>
import { ref } from "vue";
const books = ref([
  {
    id: 1,
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    publicationYear: 1960,
  },
  {
    id: 2,
    title: "1984",
    author: "George Orwell",
    genre: "Dystopian",
    publicationYear: 1949,
  },
  {
    id: 3,
    title: "The Great Gatsby",
    author: "F. Scott Fitzgerald",
    genre: "Classic",
    publicationYear: 1925,
  },
  {
    id: 4,
    title: "Pride and Prejudice",
    author: "Jane Austen",
    genre: "Romance",
    publicationYear: 1813,
  },
  {
    id: 5,
    title: "The Catcher in the Rye",
    author: "J.D. Salinger",
    genre: "Literary Fiction",
    publicationYear: 1951,
  },
]);
</script>

<template>
  <h1 class="text-slate-900 text-3xl font-bold mb-10">Book List</h1>
  <div
    class="max-w-[700px] mx-auto flex flex-wrap items-center justify-center gap-7"
  >
    <div
      class="text-slate-900 text-center"
      v-for="{ id, title, author, genre, publicationYear } in books"
      :key="id"
    >
      <h1 class="text-xl font-semibold">{{ title }}</h1>
      <h2>By {{ author }}</h2>
      <p class="font-semibold text-green-600">{{ genre }}</p>
      <p>Puplished in {{ publicationYear }}</p>
    </div>
  </div>
</template>
