<template>
  <!-- Hero -->
  <header class="masthead dark-overlay">
    <div class="container">
      <div class="intro-text">
        <div class="intro-heading text-uppercase">{{ websiteWelcomeText }}</div>
        <div class="intro-lead-in">{{ websiteWelcomeText2 }}</div>
        <a class="btn btn-primary btn-xl text-uppercase js-scroll-trigger" :href="websiteWelcomeButtonLink">{{ websiteWelcomeButtonText }}</a>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';

const websiteWelcomeText = ref('');
const websiteWelcomeText2 = ref('');
const websiteWelcomeButtonLink = ref('');
const websiteWelcomeButtonText = ref('');

onMounted(async () => {
  const response = await fetch('/config.json');
  const data = await response.json();
  websiteWelcomeText.value = data.websiteWelcomeText;
  websiteWelcomeText2.value = data.websiteWelcomeText2;
  websiteWelcomeButtonLink.value = data.websiteWelcomeButtonLink;
  websiteWelcomeButtonText.value = data.websiteWelcomeButtonText;
});
</script>

<style scoped>
header.masthead.dark-overlay {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url(../img/header-bg.jpg);
}

/* header.masthead {
  position: relative;
}

.dark-overlay:before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: #002f4b;
  opacity: .6;
  pointer-events: none;
} */
</style>
