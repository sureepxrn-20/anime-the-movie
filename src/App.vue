<script setup>
import Navbar from './components/MyNavbar.vue';
import Card from './components/MyCard.vue';
import content from './content.json';
import Header from './components/Header.vue';
</script>

<template>
  <body>
  <Navbar />
  <Header />
  <div className="grid-container">
    <Card
      v-for="item in content"
      :key="item.id"
      :id="item.id"
      :name="item.name"
      :images="item.images"
      :story="item.story"
    />
  </div>
</body>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Anuphan:wght@100..700&display=swap');
  *{
  font-family: "Anuphan", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}
body{
  background-color: #f6cd62;
}
  .grid-container {
    display: grid;
    grid-column-gap: 0.5rem;
    grid-row-gap: 0.5rem;
  }
  @media (min-width: 576px) {
    .grid-container{grid-template-columns: repeat(1,1fr);}
  }
  @media (min-width: 992px) {
    .grid-container{grid-template-columns: repeat(3,1fr);}
  }
</style>
