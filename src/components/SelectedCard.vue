<script setup>
import { watch } from "vue";

const props = defineProps({
  card: {
    type: Object,
    required: true,
  },
});
watch(props.card, (newVal) => {
  console.log(newVal);
});
</script>

<template>
  <div class="w-[80%] mx-auto mt-4 p-4 border rounded-xl shadow-md">
    <div class="text-lg text-gray-200 text-center tracking-wider">
      Cartela {{ card?.id }}
    </div>
    <div
      v-if="false"
      class="grid grid-cols-5 text-center font-bold text-xl mb-2"
    >
      <div v-for="letter in ['B', 'I', 'N', 'G', 'O']" :key="letter">
        {{ letter }}
      </div>
    </div>
    <div class="grid grid-cols-5 gap-1">
      <div
        v-for="key in ['b1', 'i1', 'n1', 'g1', 'o1']"
        :key="key"
        class="bingo-cell"
      >
        {{ card[key] }}
      </div>

      <div
        v-for="key in ['b2', 'i2', 'n2', 'g2', 'o2']"
        :key="key"
        class="bingo-cell"
      >
        {{ card[key] }}
      </div>

      <div
        v-for="key in ['b3', 'i3', 'n3', 'g3', 'o3']"
        :key="key"
        class="bingo-cell"
      >
        <span v-if="key === 'n3'" class="text-gray-500 font-medium">★ </span>
        <span class="text-lg font-semibold text-gray-800" v-else>{{
          card[key]
        }}</span>
      </div>

      <div
        v-for="key in ['b4', 'i4', 'n4', 'g4', 'o4']"
        :key="key"
        class="bingo-cell"
      >
        {{ card[key] }}
      </div>

      <div
        v-for="key in ['b5', 'i5', 'n5', 'g5', 'o5']"
        :key="key"
        class="bingo-cell"
      >
        {{ card[key] }}
      </div>
    </div>
  </div>
</template>

<style scoped>
.bingo-cell {
  @apply flex items-center justify-center w-12 h-8 text-lg font-semibold text-gray-800 bg-gray-200 border-2 border-white rounded-lg;
}
</style>
