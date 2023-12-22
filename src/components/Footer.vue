<template>
  <footer class="footer">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-4">
          <span class="copyright js-copyright">Copyright &copy; {{ companyName }} {{ currentYear }}</span>
        </div>
        <div class="col-md-4">

          <ul class="list-inline social-buttons">
            <li class="list-inline-item" v-for="socialMedia in websiteFooterSocialMediaLine1">
              <a v-if="socialMedia.link" :href="socialMedia.link" target="_blank" :title="socialMedia.name">
                <i class="fab" :class="socialMedia.icon"></i>
              </a>
            </li>
          </ul>

          <ul class="list-inline social-buttons">
            <li class="list-inline-item" v-for="socialMedia in websiteFooterSocialMediaLine2">
              <a v-if="socialMedia.link" :href="socialMedia.link" target="_blank" :title="socialMedia.name">
                <i class="fab" :class="socialMedia.icon"></i>
              </a>
            </li>
          </ul>
        </div>

        <div class="col-md-4">
          <ul class="footer-list quicklinks">
            <li class="" v-for="websiteFooterMenuItem of websiteFooterMenuItems">
              <a :href="websiteFooterMenuItem.link">{{ websiteFooterMenuItem.name }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { companyName, websiteFooterMenuItems, websiteFooterSocialMediaLine1, websiteFooterSocialMediaLine2 } from '../../public/config.json';
const currentYear = new Date().getFullYear();
const icons = [
  'fa-facebook-f',
  'fa-twitter',
  'fa-linkedin-in',
  'fa-instagram',
  'fa-reddit-alien',
  'fa-github-alt',
  'fa-patreon',
];
</script>

<style scoped>
.footer-list {
  list-style: none;
  padding-left: 0;
}

ul.social-buttons {
  margin-bottom: 8px;
}

.footer ul.quicklinks {
  font-weight: 600;
  line-height: 30px;
}

.footer {
  box-shadow: 0px -4px 10px 0px rgba(0, 0, 0, 0.05);
}
</style>
