<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import Footer from './components/Footer.vue';
</script>

<template>
  <Menu />
  <RouterView />
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
  --text-color: #fff7f3;

  --main-gradient: linear-gradient(60deg, #f79533, #f37055, #ef4e7b, #a166ab, #5073b8, #1098ad, #07b39b, #6fba82);
  --purple-color: #a166ab;
  --purple-color-2: #330a3b;
}

* {
  margin: 0;
  padding: 0;

  box-sizing: border-box;
  font-family: 'sansita', sans-serif;

  text-decoration: none;
}

body {
  color: var(--text-color);
  background: var(--dark-color-2);

  margin: 30px;

  overflow-x: hidden;
}

button {
  appearance: none;
  border: none;
  outline: none;
  background: none;

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
</style>