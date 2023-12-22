<template>
  <footer class="footer">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-4">
          <span class="copyright js-copyright">Copyright &copy; Webtech {{ currentYear }}</span>
        </div>
        <div class="col-md-4">
          <ul class="list-inline social-buttons">
            <li class="list-inline-item">
              <a href="https://twitter.com/Webtech9" target="_blank" title="Twitter">
                <i class="fab fa-twitter"></i>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://github.com/webtechca" target="_blank" title="Github">
                <i class="fab fa-github-alt"></i>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://www.patreon.com/webtech" target="_blank" title="Patreon">
                <i class="fab fa-patreon"></i>
              </a>
            </li>
          </ul>
          <ul class="list-inline social-buttons">
            <!-- <li class="list-inline-item">
              <a href="#" target="_blank" title="">
                <i class="fab fa-linkedin-in"></i>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#" target="_blank" title="">
                <i class="fab fa-reddit-alien"></i>
              </a>
            </li> -->
            <li class="list-inline-item">
              <a href="https://www.instagram.com/webtechca1" target="_blank" title="Instagram">
                <i class="fab fa-instagram"></i>
              </a>
            </li>
          </ul>
        </div>
        <div class="col-md-4">
          <ul class="footer-list quicklinks">
            <li class="">
              <a href="/">Webtech Solutions</a>
            </li>
            <li class="">
              <a href="/#services">Services</a>
            </li>
            <li class="">
              <a href="/#contact">Contact</a>
            </li>
            <li class="">
              <a href="/policy">Terms of Use</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const currentYear = new Date().getFullYear();
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
  box-shadow: 0px -4px 10px 0px rgba(0,0,0,0.05);
}
</style>
