<template>
    <Header />
    <template v-if="isPolicy">
      <PolicyContent />
    </template>
    <template v-else-if="isError404">
      <Error404 />
    </template>
    <template v-else>
      <Hero />
      <Services />
      <!-- <Clients /> -->
      <Contact />
    </template>
    <Footer />
</template>

<script setup lang="ts">
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Services from './components/Services.vue';
import Clients from './components/Clients.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import Error404 from './components/Error404.vue';
import PolicyContent from './components/PolicyContent.vue';
import { ref } from 'vue';
import { websiteRoutes } from '../public/config.json';

// const routes : { [key: string]: string } = {
//   '/': 'Home',
//   'policy': 'Policy',
// }
const routes : { [key: string]: string } = websiteRoutes;

const currentPath = ref(window.location.hash);
let currentView = routes[currentPath.value || '#'] || 'Error404';
const isPolicy = ref(currentView === 'Policy');
const isError404 = ref(currentView === 'Error404');
  console.log('currentView', currentView);

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
  // currentPath.value = window.location.pathname
  currentView = routes[currentPath.value || '#'] || 'Error404';
  isPolicy.value = currentView === 'Policy';
  isError404.value = currentView === 'Error404';
  console.log('currentView', currentView);
});

// if (currentPath.value.includes('#page-')) {
//   const currentView = routes[currentPath.value.replace('#page-', '') || '/'] || 'Error404';
//   isPolicy = currentView === 'Policy';
//   isError404 = currentView === 'Error404';
//   console.log('currentView', currentView);
// }

// const currentView = routes[currentPath.value.slice(1) || '/'] || 'Error404';
// const currentView = routes[currentPath.value || '#'] || 'Error404';
// isPolicy = currentView === 'Policy';
// isError404 = currentView === 'Error404';
// console.log('currentView', currentView);
</script>

<style>
@font-face {
  font-family: Montserrat;
  src: url(/fonts/Montserrat/Montserrat-VariableFont_wght.ttf);
}
@font-face {
  font-family: 'Kaushan Script';
  src: url(/fonts/KaushanScript-Regular.ttf);
}
@font-face {
  font-family: 'Droid Serif';
  src: url(/fonts/droid-serif/DroidSerif-Regular.ttf);
}
@font-face {
  font-family: 'Roboto Slab';
  src: url(/fonts/Roboto_Slab/RobotoSlab-VariableFont_wght.ttf);
}

input[type=text].active-cyan:focus {
  border: 1px solid #4dd0e1;
  box-shadow: 0 0 0 1px #4dd0e1;
}

input[type=text].active-green:focus {
  border: 1px solid #76b852;
  box-shadow: 0 0 0 1px #76b852;
}

.space-below {
  margin-bottom: 30px;
}

.space-above {
  margin-top: 30px;
}

.space-above-big {
  margin-top: 60px;
}

*[href*="000webhost"],
*[src*="000webhost"],
*[title*="000webhost"],
*[alt*="000webhost"] {
  display: none;
}
</style>
