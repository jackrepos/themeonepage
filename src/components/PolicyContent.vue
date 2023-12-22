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
import { ref, onMounted } from 'vue';

const websitePolicyText = ref('');
const websitePolicyTitle = ref('');

onMounted(async () => {
  const response = await fetch('/config.json');
  const data = await response.json();
  websitePolicyText.value = data.websitePolicyText;
  websitePolicyTitle.value = data.websitePolicyTitle;
});
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