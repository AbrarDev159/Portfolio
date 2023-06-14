<script setup lang="ts">
  import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav class="navbar navbar-expand-sm bg-body-tertiary">
    <div class="container-fluid">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav mx-auto">
          <RouterLink class="nav-link" :class="{ 'active': $route.path === '/' }" aria-current="page" to="/">Home</RouterLink>
          <RouterLink class="nav-link" :class="{ 'active': $route.path === '/blog' }" to="/blog">Blog</RouterLink>
        </div>
      </div>
    </div>
  </nav>

  <RouterView />
</template>

<style>
  .nav-link.active {
    text-decoration: underline
  }
</style>