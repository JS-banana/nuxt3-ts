<template>
  <div class="app">
    <header>
      <div class="title">
        <h1>Remote Developer Jobs</h1>
      </div>
      <div class="order">
        <button @click="handleClick('title')">Order by title</button>
        <button @click="handleClick('salary')">Order by salary</button>
        <button @click="handleClick('location')">Order by location</button>
      </div>
    </header>
    <JobList :jobs="jobs" :order="order" />
  </div>
</template>
<script lang="ts" setup>
import { ref } from '#imports'
import Job from '@/types/Jobs'
import OrderTerm from '@/types/OrderItems'
import { useLazyFetch } from '#app'

const { data } = useLazyFetch('https://api.github.com/orgs/nuxt')
console.log('useLazyFetch=====>', data)

const jobs = ref<Job[]>([
  {
    title: 'React developer',
    location: 'New York',
    salary: 30000,
    id: '1',
  },
  { title: 'Nodejs developer', location: 'London', salary: 40000, id: '2' },
  { title: 'Flutter developer', location: 'Lagos', salary: 35000, id: '3' },
  { title: 'Vuejs developer', location: 'Boston', salary: 21000, id: '4' },
  {
    title: 'Svelte developer',
    location: 'San Francisco',
    salary: 32000,
    id: '5',
  },
])
const order = ref<OrderTerm>('title')
const handleClick = (term: OrderTerm) => (order.value = term)
</script>
<style>
header {
  text-align: center;
}
header .order {
  margin-top: 20px;
}
button {
  margin: 0 10px;
  color: #1195c9;
  border: 3px solid #1195c9;
  background: #d5f0ff;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
}
header .title {
  display: flex;
  justify-content: center;
}
header img {
  width: 60px;
  margin-right: 20px;
}
header h1 {
  font-size: 3em;
}
</style>
