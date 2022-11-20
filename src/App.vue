<script setup>
import { RouterLink, RouterView } from "vue-router";
import { ref } from "vue";
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";
import Cards from "./components/Cards.vue";
import Hero from "./components/Hero.vue";
import Skils from "./components/Skils.vue";

const isLogic = ref(true);
const handleClick = () => {
  isLogic.value = !isLogic.value;
};
</script>

<template>
  <div class="container">
    <header>
      <div class="logo">Farik</div>

      <nav :class="{ navToggle: isLogic }">
        <ul>
          <li><a href="#home" @click="handleClick">Home</a></li>
        </ul>
        <ul>
          <li><a href="#about" @click="handleClick">About</a></li>
        </ul>
        <ul>
          <li><a href="#project" @click="handleClick">Project</a></li>
        </ul>
        <ul>
          <li><a href="#contact" @click="handleClick">Contact</a></li>
        </ul>

        <!-- <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/project">Project</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink> -->
      </nav>
      <img
        @click="handleClick"
        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAABmJLR0QA/wD/AP+gvaeTAAABrElEQVR4nO3aP0tbYRTH8e9JS6Np3Yo4qAQ6ZOtmu4lTX0UHFztY/yxCX4OTQwUplIL0BfQFpOIoFDrXgggpQehWKkTQ5DkdMpecmHtzr/H3gWf7cfndex/Icw8BERERkXvKokF/X1/B0ss8y2TC6eCPDm3r7G8k/jB0zb16HVITj+WLd/0cWIskKzk3KYbh8WiQ7y8s45VXuJd7F5j/plP7aO9+XhZdRUREyi78M0j/0DRP+c8OCWgD3SwvOgOcAn5H1inwJMsH8KIENzXsWorcWPRU9x34BKwE80U7pt9ZRERE/i8+ETp4Nkuvu4370zwLjcytR4WmbbS+ROJDTIUXPwOvb11svBKV1LC37bNBwSE+bPzPKI3G7JpknUgwPuD06g52c4J5ph8ZufB0Ypvti6JriIiITIgp4Ij+xLXoWd+glYCvQDXLBzCxQ9GoKv2neld2QJOMd4CIiMgEis8Edxsz1K5WMWp5FspEz77Zdus4Eh1mKPoBeHPrUuPV5QENW/91PihY9n975C4+FO1M7/D46geJuRz7jM6si/eatt4e+PZFRERE7rV/k80ztByBEj4AAAAASUVORK5CYII="
      />
    </header>
  </div>
  <Hero id="home" />
  <!-- <RouterView  /> -->

  <About id="about" />
  <Skils />
  <div class="getColor">
    <h1 class="project" id="project">Projects</h1>
    <div class="cards-container">
      <Cards
        image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
        title="Chat application"
        lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
      />
      <Cards
        image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
        title="Todo App"
        lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
        link="#chatApp"
      />
      <Cards
        image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
        title="Spotify landing page"
        lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
      />
      <Cards
        image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
        title="Recipe website"
        lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
      />
    </div>
  </div>

  <Contact id="contact" />
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  background-color: #2b2b2b;
  padding: 17px;
}
.logo {
  font-family: "Pacifico", cursive;
  font-weight: 400;
  color: #ffe0b2;
  font-size: 2rem;
}
img {
  display: none;
}
nav {
  display: flex;
}
li {
  list-style: none;
}
a {
  font-size: 1.5rem;
  text-decoration: none;
  padding-right: 23px;
  color: aliceblue;
}
a:hover {
  color: #ffe0b2;
}
.cards-container {
  display: flex;
}
.getColor {
  background-color: #2b2b2b;
}
h1 {
  text-align: center;
  color: #ffe0b2;
  padding: 50px;
}
@media screen and (max-width: 992px) {
  header {
    background-color: #2b2b2b;
    padding: 17px;
  }
  nav {
    display: flex;
    flex-direction: column;
    text-align: center;
    padding: 17px;
  }

  .logo {
    font-family: "Pacifico", cursive;
    font-weight: 400;
    color: #ffe0b2;
    font-size: 2rem;
  }
  img {
    display: block;
    height: 40px;
    width: 40px;
  }
  a {
    display: block;
    padding: 70px;
    text-align: center;
    font-size: 1.5rem;
    text-decoration: none;
    color: aliceblue;
  }
  a:hover {
    color: #ffe0b2;
  }

  .navToggle {
    display: none;
  }

  .getColor {
    background-color: #2b2b2b;
  }
  h1 {
    text-align: center;
    color: #ffe0b2;
    padding: 50px;
  }
  .cards-container {
    display: flex;
    flex-direction: column;
  }
}
</style>
