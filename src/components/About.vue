<template>
  <div class="container">
    <h1>About Me</h1>
    <div class="img-container">
      <img
        src="../foto/fotoPerso.jpg"
        alt="Farik photo"
        class="circular-square"
      />
    </div>

    <p class="text">
      I'm a web developer with a focus on Javascript and Vue.js , but still
      exploring other technologies and frameworks that catch my interest! if
      you're looking for a developer to add to your team,I'd love to hear from
      you!
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
.container {
  background-color: #2b2b2b;
  /* height: 400px; */
}

.text {
  color: #e7e7e7;
  font-size: 25px;
  padding: 50px;
}
.img-container {
  display: flex;
  justify-content: center;
}
.circular-square {
  border-top-left-radius: 50% 50%;
  border-top-right-radius: 50% 50%;
  border-bottom-right-radius: 50% 50%;
  border-bottom-left-radius: 50% 50%;
  height: 500px;
  width: 500px;
}
h1 {
  text-align: center;
  color: #ffe0b2;
  padding: 70px;
}
@media screen and (max-width: 992px) {
  .container {
    background-color: #2b2b2b;
    /* height: 400px; */
  }

  .text {
    color: #e7e7e7;
    font-size: 25px;
    padding: 50px;
  }
  .img-container {
    display: flex;
    justify-content: center;
  }
  .circular-square {
    border-top-left-radius: 50% 50%;
    border-top-right-radius: 50% 50%;
    border-bottom-right-radius: 50% 50%;
    border-bottom-left-radius: 50% 50%;
    height: 200px;
    width: 200px;
  }
  h1 {
    text-align: center;
    color: #ffe0b2;
    padding: 70px;
  }
}
</style>
