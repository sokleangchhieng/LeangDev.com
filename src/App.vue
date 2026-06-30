<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Sidebar from './components/Sidebar.vue';
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <RouterLink to="/" class="navbar-brand fw-bold logo">LeangDev</RouterLink>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
              aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <RouterLink to="/" class="nav-link fw-bold" exact-active-class="active">Home</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink to="/resume" class="nav-link fw-bold" exact-active-class="active">Resume</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink to="/experience" class="nav-link fw-bold" exact-active-class="active">Portfolio</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink to="/contact" class="nav-link fw-bold" exact-active-class="active">Contact</RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <main class="main-content">
    <div class="container py-3">
      <div class="custom-row">
        <div class="sidebar-wrapper">
          <Sidebar />
        </div>
        
        <div class="content-wrapper">
          <RouterView />
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.logo{
  color: #9024b6;
}
.navbar-nav .nav-link.active {
  color: #9024b6 !important;
  font-weight: bold;
}

.navbar-nav .nav-link:hover {
  color: #9024b6;
}
.custom-row {
  display: flex;
  gap: 20px;
  align-items: stretch;
}

.sidebar-wrapper {
  flex: 0 0 280px;
}

.content-wrapper {
  flex: 1;
  min-width: 0;
}
</style>
