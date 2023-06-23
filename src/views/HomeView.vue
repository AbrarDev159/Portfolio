<script setup lang="ts">
  import { ref } from 'vue'
  import jsonData from '@/data/projects.json'

  const items = ref(jsonData)
</script>

<template>
  <div class="row row-cols-1 row-cols-lg-2 g-4 m-2">
    <div v-for="item in items" :key="item.id" class="col">
      <div class="card h-100">
        <!-- <img src="..." class="card-img-top" alt="..."> -->
        <div class="card-body">
          <h5 class="card-title">{{ item.name }}</h5>
          <p class="card-text">{{ item.technology }}</p>
          <p class="card-text">{{ item.description }}</p>
          <p class="card-text">Github: <a :href="item.github" target="_blank" rel="noopener noreferrer">{{ item.github }}</a></p>
          <p class="card-text">Website: <a :href="item.website" target="_blank" rel="noopener noreferrer">{{ item.website }}</a></p>
        </div>
      </div>
    </div>
  </div>
</template>
