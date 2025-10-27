<script setup>
defineProps({
  wallet: Number,
  game: Object,
});
</script>

<template>
  <div class="flex justify-between items-center gap-1">
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 h-14 flex justify-center items-center text-2xl font-extrabold text-red-500"
    >
      {{ game?.count || 0 }}
    </div>
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 h-14 flex flex-col justify-center items-center text-lg font-bold text-red-500"
    >
      <span class="font-bold">Wallet</span>
      <span>{{ wallet }}</span>
    </div>
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 h-14 flex flex-col justify-center items-center text-lg text-red-500"
    >
      <span class="font-bold">Stake</span>
      <span>10</span>
    </div>
  </div>
</template>
