<template>
  <div class="rootDiv">
    <img
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRP_dcjLPT3bcNrMRUB5MY9r83YHM64MOsVOA&usqp=CAU"
      alt=""
    />
    <h2>Richard`s Travel Blog</h2>
    <div class="links">
      <p><RouterLink :to="`/contact`">Contact</RouterLink></p>
      <a href="">Add post</a>
      <a href="">Login/Logout</a>
    </div>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router';
export default {
  components: {
    RouterLink
  }
};
</script>

<style scoped>
a {
  color: white;
  text-decoration: none;
}
.links {
  display: flex;
  justify-content: end;
  margin-left: 500px;
}
div {
  align-items: center;
  text-align: center;
  display: flex;
  gap: 20px;
}
img {
  border-radius: 50%;
  margin-left: 10px;
  width: 4%;
}
.rootDiv {
  min-width: 800px;
}
</style>
