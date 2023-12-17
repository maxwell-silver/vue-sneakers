<script setup lang="ts">
defineProps<{
  title: string
  price: number
  isAdded: boolean
}>()
</script>

<template>
  <div class="border-2 rounded mb-2 p-4 text-slate-700">
    <p>
      Товар: <span class="font-bold">{{ title }}</span>
    </p>
    <p>
      Цена: <span class="font-bold">{{ price }}</span>
    </p>
    <p>Добавлен: {{ isAdded }}</p>
  </div>
</template>
