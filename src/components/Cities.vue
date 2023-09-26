<template>
  <div class="cityCards">
    <CityCards
      imageURL="https://assets.cntraveller.in/photos/60ba13c3556f29fbec5f2281/16:9/w_1920,h_1080,c_limit/Tokyo-Shibuya-neon-lights.jpg"
      cityName="Tokyo"
      visitingDate="2013.07.23"
    />
    <CityCards
      imageURL="https://vegasexperience.com/wp-content/uploads/2023/01/Photo-of-Las-Vegas-Downtown-1920x1280.jpg"
      cityName="Las Vegas"
      visitingDate="2014.07.12"
    />
    <CityCards
      imageURL="https://cdn.wallpapersafari.com/95/17/jA06IS.jpg"
      cityName="Paris"
      visitingDate="2015.09.21"
    />
  </div>
  <div class="cityCards">
    <CityCards
      imageURL="https://upload.wikimedia.org/wikipedia/commons/e/e2/Stockholm_Skyline_At_Night_%2891983391%29.jpeg"
      cityName="Stockholm"
      visitingDate="2017.02.06"
    />
    <CityCards
      imageURL="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTv8n226JKT5jY2PmoIiOdTqkzo4EGJYUGwHw&usqp=CAU"
      cityName="San Diego"
      visitingDate="2017.08.17"
    />
    <CityCards
      imageURL="https://travel2next.com/wp-content/uploads/sydney-opera-house-at-night.jpg"
      cityName="Sydney"
      visitingDate="2019.05.09"
    />
  </div>
  <div class="map">
    <Map />
  </div>
</template>

<script>
import Map from './Map.vue';
import CityCards from '../components/CityCards.vue';

export default {
  components: { CityCards, Map }
};
</script>

<style scoped>
.map {
  width: 1110px;
  height: 500px;
}
.cityCards {
  gap: 80px;
}
div {
  margin-top: 10px;
  margin-left: 15px;
  width: 50vw;
  height: auto;
  display: inline-flex;
  gap: 20px;
}
</style>
