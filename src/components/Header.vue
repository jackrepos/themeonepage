<template>
  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top" :class="{ 'navbar-shrink': forceShrink }" id="mainNav">
    <div class="container">
      <a class="navbar-brand js-scroll-trigger" href="/" id="companyName">{{ companyName }}</a>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
        <i class="fas fa-bars"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav text-uppercase ml-auto">
          <li class="nav-item" v-for="menuItem of websiteMenuItems">
            <a class="nav-link" :class="{ 'js-scroll-trigger': menuItem.name === 'Contact' }" :href="menuItem.link">{{ menuItem.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { companyName, websiteMenuItems } from '../../public/config.json';

const forceShrink = ref(false);

const shouldShrink = () => {
  const scrollY = window.scrollY;
  const shrinkHeight = 100;
  return scrollY > shrinkHeight;
};

onMounted(() => {
  forceShrink.value = shouldShrink();

  window.addEventListener('scroll', () => {
    forceShrink.value = shouldShrink();
  });
});
</script>

<style scoped>
#mainNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
}
</style>
