<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import Footer from './components/Footer.vue';
import scrollToTop from './components/scrollToTop.vue';
</script>

<template>
  <Menu />
  <RouterView />
  <ScrollToTop />
  <Footer />
</template>


<style lang="scss">
:root {
  --background-color-2: #C599B6;
  --pastel-color-1: #9d7f84;
  --pastel-color-2: #FAD0C4;
  --text-color: #fff7f3;

  --grey: #64748b;
  --dark: #1e293b;
  --dark-alt: #334155;
  --light: #f1f5f9;
  --sidebar-width: 300px;

  --dark-color: #1A1A1D;
  --dark-color-2: #1e1e1e;
  --background-color: #3B1C32;
  --main-color: #6A1E55;
  --pastel-color: #A64D79;

  --main-gradient: linear-gradient(60deg, #f79533, #f37055, #ef4e7b, #a166ab, #5073b8, #1098ad, #07b39b, #6fba82);
  --purple-color: #a166ab;
  --purple-color-2: #330a3b;
}

* {
  margin: 0;
  padding: 0;

  box-sizing: border-box;

  text-decoration: none;
}

body {
  color: var(--text-color);
  background: var(--dark-color-2);

  margin: 30px;

  /*font-family: "Bitcount Prop Single", system-ui;
  font-optical-sizing: auto;
  font-style: normal;
  font-variation-settings:
    "slnt" 0,
    "CRSV" 0.5,
    "ELSH" 0,
    "ELXP" 0;*/

  overflow-x: hidden;
}

button {
  /*font-family: "Bitcount Prop Single", system-ui;
  font-optical-sizing: auto;
  font-style: normal;
  font-variation-settings:
    "slnt" 0,
    "CRSV" 0.5,
    "ELSH" 0,
    "ELXP" 0;*/

  background: none;
  border: none;
  outline: none;
  appearance: none;

  cursor: pointer;
}

li {
  list-style-type: none;
}

@media screen and (max-width: 768px) {
  body {
    margin: 15px;
  }
}

/*========================== ICONS =============================*/
.fa-instagram {
  color: var(--white);
  background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);

  border-radius: 50%;
}

.instagram-text {
  color: var(--white);
  background-image: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);

  background-clip: text;
  --webkit-background-clip: text;
  --webkit-text-fill-color: transparent;
}

.fa-twitter {
  color: #00acee;
}

.fa-snapchat {
  color: #000;
  background: var(--white);
}

.fa-github {
  color: var(--white);
  background: #000;

  border-radius: 25px;
}

.fa-pinterest {
  color: #c8232c;
  background: var(--white);

  border-radius: 50%;
}

.fa-linkedin,
.fa-linkedin-in {
  color: var(--white);
  background: #0072b1;
}

.fa-whatsapp {
  color: var(--white);
  background: #25d366;

  border-radius: 25px;
}

.fa-facebook {
  color: var(--white);
  background: #4267b2;

  border-radius: 25px;
}

.fa-youtube {
  color: #c4302b;
}

.fa-tiktok {
  color: #111111;
  filter: drop-shadow(2px 0 0 #fd3e3e) drop-shadow(-2px -2px 0 #4de8f4);
}

.fa-spotify {
  color: #1db954;
  background: #000;

  border-radius: 50%;
}

.g-blue {
  color: #4285f4;
}

.o-red {
  color: #db4437;
}

.o-yellow {
  color: #f4b400;
}

.l-green {
  color: #0f9d58;
}

.e-red {
  color: #db4437;

  display: inline-block;

  transform: rotate(-20deg);
}

.fa-reddit {
  color: #ff4500;
  background: var(--white);
  border-radius: 50%;
}

.fa-quora {
  color: #a82400;
}

.fa-podcast {
  color: var(--white);
}

.fa-imdb {
  color: #f5c518;
}

.fa-hashnode {
  color: #2962ff;
}

.fa-deviantart {
  color: #05cc47;
}

.fa-artstation {
  color: #1caad9;
}

.fa-x-twitter {
  color: #1da1f2;
}

</style>