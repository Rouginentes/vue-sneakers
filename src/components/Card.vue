<script setup>
defineProps({
  imageUrl: String,
  price: Number,
  title: String,
  isAdded: Boolean,
  isFavorite: Boolean,
})
</script>

<template>
  <div
    class="relative bg-white border border-slate-100 rounded-3xl p-8 cursor-pointer hover:-translate-y-2 hover:shadow-xl transition"
  >
    <img
      class="cursor-pointer absolute top-8 left-8"
      :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
      alt="like 1"
    />
    <img :src="imageUrl" alt="sneakers" />
    <p>{{ title }}</p>

    <div class="flex justify-between mt-5">
      <div class="flex flex-col">
        <span class="text-slate-400">Цена:</span>
        <b>{{ price }}</b>
      </div>

      <img :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="" />
    </div>
  </div>
</template>
