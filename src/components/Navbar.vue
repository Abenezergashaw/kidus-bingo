<script setup>
defineProps({
  wallet: Number,
  game: Object,
  stake: Number,
});
</script>

<template>
  <div class="flex justify-between items-center gap-1">
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 py-1 flex justify-center items-center h-12 text-sm font-extrabold text-gray-800"
    >
      {{ game?.count || 0 }}
    </div>
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 py-1 flex flex-col justify-center items-center h-12 text-sm font-bold text-gray-800"
    >
      <span class="font-bold">Wallet</span>
      <span>{{ wallet }}</span>
    </div>
    <div
      class="bg-white rounded-lg border-2 border-gray-300 flex-1 py-1 flex flex-col justify-center items-center h-12 text-sm text-gray-800"
    >
      <span class="font-bold">Stake</span>
      <span>{{ stake }}</span>
    </div>
  </div>
</template>
