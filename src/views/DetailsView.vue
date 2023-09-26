<template>
  <div class="header">
    <TheHeader />
  </div>
  <div class="arrow">
    <h1><RouterLink :to="`/`">&#8592; Back to home page</RouterLink></h1>
  </div>
  <div class="title">
    <h1>Welcome to {{ city }}</h1>
  </div>
  <div class="date">
    <h2>{{ visitingDate }}</h2>
  </div>
  <div>
    <img :src="`${image} `" alt="" class="theImage" />
  </div>
  <div class="text">
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur qui esse, quos corporis
      sequi provident voluptatem incidunt ut velit ducimus maxime dolor aut minima assumenda
      pariatur fugiat est totam. Itaque! Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Nobis et eligendi reiciendis beatae at omnis maiores voluptas nulla necessitatibus inventore,
      fugit modi voluptatibus iste aliquam mollitia ipsa. Optio, dolores earum! Lorem ipsum dolor
      sit amet, consectetur adipisicing elit. Quaerat nihil est adipisci quasi ullam distinctio
      similique fugiat, minus fugit impedit provident, hic sunt voluptatum voluptate velit voluptas
      enim illum amet? Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus quis
      numquam magni consectetur, recusandae officia provident facilis? Numquam unde, quaerat placeat
      magnam consectetur minus illo porro blanditiis reprehenderit eos. Placeat? Lorem ipsum dolor
      sit amet consectetur adipisicing elit. Quis, enim reiciendis fuga quo ea distinctio temporibus
      commodi quaerat perspiciatis, molestiae nesciunt aperiam dignissimos doloremque eligendi nisi
      consequatur, illo impedit praesentium.
    </p>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router';
import TheHeader from '../components/TheHeader.vue';
export default {
  components: { TheHeader, RouterLink },
  data() {
    return {
      city: this.$route.query.name,
      image: this.$route.query.image,
      visitingDate: this.$route.query.visitingDate
    };
  }
};
</script>

<style scoped>
.header {
  height: 80px;
  width: 100vw;
  display: flex;
  margin: 0 auto;
  border-bottom: 3px solid white;
  border-top: 3px solid white;
}

a {
  text-decoration: none;
  color: white;
}
.location {
  text-align: center;
}
.text {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 50px;
  width: 90vw;
  height: 200px;
}
.theImage {
  margin-left: 250px;
  width: 700px;
  height: 400px;
}
.date {
  text-align: center;
}
.title {
  text-align: center;
}
</style>
