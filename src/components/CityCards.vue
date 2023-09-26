<template>
  <div class="cityCard">
    <RouterLink :to="`/details?name=${cityName}&image=${imageURL}&visitingDate=${visitingDate}`"
      ><img :src="`${imageURL} `" class="cityImage"
    /></RouterLink>
    <div class="details">
      <h2>
        City name :
        <RouterLink
          :to="`/details?name=${cityName}&image=${imageURL}&visitingDate=${visitingDate}`"
          >{{ cityName }}</RouterLink
        >
      </h2>
      <h2>Date visited : {{ visitingDate }}</h2>
    </div>
    <div class="author">
      <p>Posted by: Richard Retter</p>
      <img
        src="https://media.glamour.com/photos/5f84aabda8de7ca88085a3d7/1:1/w_993,h_993,c_limit/Jensen%20Ackles.jpg"
        alt=""
        class="authorImage"
      />
    </div>
  </div>
</template>

<script>
// <img :src="`${imageURL} `" alt="" class="cityImage" />
// City name : {{ cityName }}
import DetailsView from '../views/DetailsView.vue';
import { RouterLink } from 'vue-router';
export default {
  props: ['cityName', 'visitingDate', 'imageURL'],
  components: {
    RouterLink,
    DetailsView
  }
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: white;
}
.authorImage {
  margin-top: 10px;
  margin-left: 10px;
  width: 30px;
  height: 30px;
}
.author {
  position: absolute;
  margin-left: 20px;
  margin-top: 300px;
}
.details {
  margin-left: 20px;
  margin-top: 150px;
  position: absolute;
}
.cityImage {
  position: relative;
  width: 300px;
  height: 150px;
}
.cityCard {
  border: 1px solid white;
  width: 400px;
  height: 400px;
}
.author {
  display: inline-flex;
}
</style>
