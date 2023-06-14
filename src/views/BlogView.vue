<script setup lang="ts">
  import { ref } from 'vue'
  import jsonData from '@/data/blogs.json'

  const blogs = ref(jsonData)
</script>

<template>
  <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4 m-2">
    <div v-for="blog in blogs" :key="blog.id" class="col">
      <div class="card h-100">
        <!-- <img src="..." class="card-img-top" alt="..."> -->
        <div class="card-body">
          <h5 class="card-title">{{ blog.name }}</h5>
        </div>
      </div>
    </div>
  </div>
</template>
