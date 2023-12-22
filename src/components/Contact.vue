<template>
    <!-- Contact -->
    <section class="page-section" id="contact">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">{{ websiteContactTitle }}</h2>
          <h3 class="section-subheading text-muted">Do not hesitate to reach out if you have any request.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12">
            <!-- <div class="alert alert-warning">Sorry, my mail server is not available at the moment! Contact me at <strong>jacques.mi@outlook.com</strong></div> -->
            <div class="alert alert-warning">If my mail server is not available at the moment, please contact me at <strong id="adminEmail">jacques.mi@outlook.com</strong></div>
        </div>
        <div class="col-lg-12">
          <!-- <form id="contactForm" name="sentMessage" novalidate="novalidate" class="js-contact-form"> -->
          <form id="contactForm" name="sentMessage" class="js-contact-form">
            <div class="row">
              <div class="col-md-6">
                <div class="form-group">
                  <input class="form-control" id="name" type="text" placeholder="Your Name *" required
                    data-validation-required-message="Please enter your name.">
                  <p class="help-block text-danger"></p>
                </div>
                <div class="form-group">
                  <input class="form-control" id="email" type="email" placeholder="Your Email *" required
                    data-validation-required-message="Please enter your email address.">
                  <p class="help-block text-danger"></p>
                </div>
                <div class="form-group">
                  <input class="form-control" id="subject" type="text" placeholder="Your Subject">
                  <p class="help-block text-danger"></p>
                </div>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <textarea class="form-control" id="message" placeholder="Your Message *" required
                    data-validation-required-message="Please enter a message."></textarea>
                  <p class="help-block text-danger"></p>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { websiteContactSchedule, websiteContactText, websiteContactTitle } from '../../public/config.json';
</script>