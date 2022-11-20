<template>
  <!-- <img :src="{ imagen }" alt="imagen" /> -->
  <div class="container">
    <div class="hero-text">
      <h2 class="hero-title hero-color">HI THERE I'M</h2>
      <h1 class="hero-name hero-color">Farik Fakhreddine</h1>
      <P class="hero-text hero-color"
        >A Front-end web Developer passionate about creating interactive
        applications and experiences on the web.</P
      >
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
@media screen and (max-width: 992px) {
  .container {
    background-color: #212121;
    height: 700px;
  }
  .hero-color {
    color: #e7e7e7;
    padding: 40px;
  }
  .hero-name {
    color: #ffe0b2;
  }
  .hero-text {
    font-size: 27px;
  }
}
</style>
