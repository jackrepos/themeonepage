<script setup lang="ts">
import Header from './components/Header.vue';
import PolicyContent from './components/PolicyContent.vue';
import Footer from './components/Footer.vue';

</script>

<template>
    <Header />
    <PolicyContent />
    <Footer />
</template>

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
