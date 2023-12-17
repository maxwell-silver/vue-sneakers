<script setup lang="ts">
import HelloBlock from './components/HelloBlock.vue'
import { v4 as uuid } from 'uuid'
import { reactive } from 'vue'

interface IGood {
  title: string
  price: number
  isAdded: boolean
  id: string
}

const goods = reactive<IGood[]>([
  { title: 'Кроссовки Puma', price: 9500, isAdded: false, id: uuid() },
  { title: 'Кроссовки Nike', price: 15000, isAdded: true, id: uuid() },
  { title: 'Кроссовки New Balance', price: 20000, isAdded: true, id: uuid() }
])
</script>

<template>
  <div v-for="good in goods" :key="good.id" class="m-4">
    <HelloBlock
      :title="good.title"
      :price="good.price"
      :is-added="good.isAdded"
    />
  </div>
</template>

<style scoped></style>
