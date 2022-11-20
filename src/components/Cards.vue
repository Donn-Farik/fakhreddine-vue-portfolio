<template>
  <div class="container">
    <v-card class="mx-auto fromCss">
      <img :src="props.image" />

      <v-card-title>
        <h2>{{ title }}</h2></v-card-title
      >

      <v-card-subtitle> {{ lorem }} </v-card-subtitle>

      <v-card-actions>
        <v-btn color="orange lighten-2" text>
          <a :href="props.link">Explor</a></v-btn
        >
      </v-card-actions>
    </v-card>
  </div>
</template>

<script setup>
const props = defineProps({
  image: {
    type: String,
  },
  title: {
    type: String,
  },
  lorem: {
    type: String,
  },
  link: {
    type: String,
  },
});
</script>

<style scoped>
img {
  height: 300px;
}
.container {
  padding: 20px;
  background-color: #2b2b2b;
}
h2 {
  margin-top: 13px;
  color: #ffe0b2;
}
.fromCss {
  margin-top: 30px;
  width: 330px;
}
a {
  text-decoration-line: none;
}
@media screen and (max-width: 992px) {
  img {
    height: 300px;
  }
  .container {
    padding: 20px;
  }
  h1 {
    margin-top: 13px;
    color: #ffe0b2;
  }
  .fromCss {
    margin-top: 30px;
  }
}
</style>
