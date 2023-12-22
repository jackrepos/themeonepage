<template>
  <!-- Hero -->
  <header class="masthead">
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
import { websiteWelcomeText, websiteWelcomeText2, websiteWelcomeButtonLink, websiteWelcomeButtonText } from '../../public/config.json';
</script>

<style scoped></style>
