<script setup>
import DrawerHead from './DrawerHead.vue'
import CartItemList from './CartItemList.vue'
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="bg-white h-full w-96 fixed right-0 top-0 z-20 p-8">
    <DrawerHead />

    <CartItemList />

    <div class="flex flex-col gap-3 mt-7">
      <div class="flex gap-2">
        <span>Итого:</span>
        <div class="flex-1 border-b border-dashed border-slate-200"></div>
        <b>12999 руб.</b>
      </div>

      <div class="flex gap-2">
        <span>Налог: 5%</span>
        <div class="flex-1 border-b border-dashed border-slate-200"></div>
        <b>900 руб.</b>
      </div>
      <button
        disabled=""
        class="mt-4 bg-lime-500 rounded-xl w-full py-3 text-white hover:bg-lime-600 active:bg-lime-700 disabled:bg-slate-300 transition cursor-pointer"
      >
        Оформить
      </button>
    </div>
  </div>
</template>
