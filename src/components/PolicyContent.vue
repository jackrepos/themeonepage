<template>
  <!-- Policy -->
  <header class="policyhead"></header>

  <section class="page-section" id="policy">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">{{ websitePolicyTitle }}</h2>
        </div>

        <div class="col-lg-12" v-html="websitePolicyText"></div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { websitePolicyText, websitePolicyTitle } from '../../public/config.json';
</script>

<style scoped>
.page-section h2.section-heading {
  margin-bottom: 30px;
}

.policyhead {
  /* background-image: url("/img/policy.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; */
  background-color: #212529;
  height: 110px;
  width: 100%;
  margin-bottom: 0px;
}
</style>