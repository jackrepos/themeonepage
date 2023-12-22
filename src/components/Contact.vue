<template>
    <!-- Contact -->
    <section class="page-section" id="contact">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">{{ websiteContactTitle }}</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12">
            <div class="alert alert-warning" v-html="contactText"></div>
        </div>
        <div class="col-lg-12">
            <div class="row">
              <div class="col-md-6">
                <div class="contact-info">{{ companyAddress }}</div>
              </div>
              <div class="col-md-6">
                <!-- <div class="form-group">
                  <textarea class="form-control" id="message" placeholder="Your Message *" required
                    data-validation-required-message="Please enter a message."></textarea>
                  <p class="help-block text-danger"></p>
                </div> -->
                <div class="contact-schedule">
                  <p class="contact-schedule-row" v-for="item in websiteContactSchedule">
                    <span class="contact-schedule-day">{{ item.day }}</span>
                    <span class="contact-schedule-hours">{{ item.hours }}</span>
                  </p>
                </div>
              </div>
            </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { websiteContactSchedule, websiteContactText, websiteContactTitle, companyEmail, companyPhone, companyAddress } from '../../public/config.json';

const contactText = websiteContactText.replace('{companyEmail}', companyEmail)
  .replace('{companyPhone}', companyPhone);
</script>

<style scoped>
.contact-schedule,
.contact-info {
    background-color: #fff;
    border-color: #fff;
    position: relative;
    padding: .75rem 1.25rem;
    margin-bottom: 1rem;
    border-radius: .25rem;
}

.contact-schedule-row {
  border-bottom: 1px solid #eee;
}

.contact-schedule-hours {
  float: right;
}
</style>