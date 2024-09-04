<script>
export default {
  props: ['id', 'name', 'images','story']
}
</script>

<template>
  <div class="card">
    <div class="image-container">
      <img v-if="images" :src="images" :alt="name">
      <div v-else class="no-image">No Image Available</div>
    </div>
    <div class="container">
      <center><h4>{{ name }}</h4></center>
      <p>เรื่องย่อ :{{ story }}</p>
    </div>
  </div>
</template>

<style scoped>
/* .container{
    background-color: #986c51;
    color: aliceblue;
} */
.card {
  border-radius: 30px;
  margin: 1rem;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  background-color: aliceblue;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.image-container {
  width: 100%;
  height: 200px; 
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; 
  margin-bottom: 20px;
  margin-top: 25px;
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit:scale-down; 
}

.no-image {
  width: 100%;
  height: 100%;
  background-color: #eaeaea;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #888;
}

.container {
  padding: 2px 16px;
}
h4{
    margin-bottom: 10px;
}
</style>
