<template>
  <!-- Clients -->
  <section class="py-5 section-clients" id="clients">
    <div class="container">
      <div class="row">
        <div class="col-md-3 col-sm-6">
          <a href="https://www.patreon.com/webtech" target="_blank">
            <img class="img-fluid d-block mx-auto" src="/img/logos/patreon.png" alt="">
          </a>
        </div>
        <div class="col-md-3 col-sm-6">
          <a href="https://github.com/webtechca" target="_blank">
            <img class="img-fluid d-block mx-auto" src="/img/logos/github.png" alt="">
          </a>
        </div>
        <div class="col-md-3 col-sm-6">
          <a href="https://twitter.com/Webtech9" target="_blank">
            <img class="img-fluid d-block mx-auto" src="/img/logos/twitter.png" alt="">
          </a>
        </div>
        <div class="col-md-3 col-sm-6">
          <a href="#">
            <img class="img-fluid d-block mx-auto" src="/img/logos/paypal.svg" alt="">
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#clients {
  padding-top: 0 !important;
}
.section-clients .img-fluid.d-block.mx-auto {
  width: 200px;
  height: auto;
}

@media (max-width: 500px) {
  #clients .col-sm-6 {
    margin-bottom: 15px;
  }
}
</style>