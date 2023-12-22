<template>
  <!-- Services -->
  <section class="page-section" id="services">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">{{ websiteServicesTitle }}</h2>
          <h3 class="section-subheading text-muted">{{ websiteServicesText }}</h3>
        </div>
      </div>
      <div class="row text-center services-row">
        <div class="col-md-4 services-card" v-for="websiteService of websiteServices">
          <div class="img-card">
            <img :src="websiteService.image" alt="">
          </div>
          <h4 class="service-heading">{{ websiteService.name }}</h4>
          <p class="text-muted" v-html="websiteService.description"></p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { websiteServices, websiteServicesText, websiteServicesTitle } from '../../public/config.json';
</script>

<style scoped>
.services-card {
  box-shadow: -4px 4px 10px 4px rgba(0, 0, 0, 0.05);
}

.services-row {
  justify-content: space-between;
}

@media (min-width: 768px) {
  .services-row .col-md-4 {
      -ms-flex: 0 0 31%;
      flex: 0 0 31%;
      max-width: 31%;
  }
}

.services-card .img-card {
  height: 200px;
  overflow: hidden;
}

.services-card .img-card img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

@media (max-width: 500px) {
  .services-card {
    box-shadow: none;
  }
}
</style>